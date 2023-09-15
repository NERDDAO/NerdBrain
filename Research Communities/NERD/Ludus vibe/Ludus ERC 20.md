Sure! Here's an example of an ERC20 token contract named 'Ludus' that interacts with an ERC721 NFT representing athlete profiles:

```solidity
pragma solidity ^0.8.21;

import 'lens/contracts/interfaces/ILens.sol';
import '@openzeppelin/contracts/token/ERC20/IERC20.sol';
import '@openzeppelin/contracts/token/ERC20/extensions/ERC20Burnable.sol';
import '@openzeppelin/contracts/access/Ownable.sol';
import '@openzeppelin/contracts/utils/math/SafeMath.sol';

contract Ludus is IERC20, ERC20Burnable, Ownable {
    using SafeMath for uint256;
    
    string private _name;
    string private _symbol;
    uint8 private _decimals;

    mapping(address => uint256) private _balances;
    mapping(address => mapping(address => uint256)) private _allowances;

    constructor() ERC20('Ludus', 'LUD') {
        _name = 'Ludus';
        _symbol = 'LUD';
        _decimals = 18;
        // Mint initial supply to the contract owner
        _mint(msg.sender, 1000000 * 10 ** uint256(decimals()));
    }

    // ERC20 transfer function
    function transfer(address recipient, uint256 amount) public virtual override returns (bool) {
        _transfer(msg.sender, recipient, amount);
        return true;
    }

    // ERC20 transferFrom function
    function transferFrom(address sender, address recipient, uint256 amount) public virtual override returns (bool) {
        _transfer(sender, recipient, amount);
        _approve(sender, _msgSender(), _allowances[sender][_msgSender()].sub(amount, 'ERC20: transfer amount exceeds allowance'));
        return true;
    }

    // ERC20 approve function
    function approve(address spender, uint256 amount) public virtual override returns (bool) {
        _approve(_msgSender(), spender, amount);
        return true;
    }
    
    // ERC20 allowance function
    function allowance(address owner, address spender) public view virtual override returns (uint256) {
        return _allowances[owner][spender];
    }

    // ERC20 total supply function
    function totalSupply() public view virtual override returns (uint256) {
        return ERC20.totalSupply();
    }

    // ERC20 balance of function
    function balanceOf(address account) public view virtual override returns (uint256) {
        return _balances[account];
    }

    // Internal transfer function with additional checks for ERC20 transfers
    function _transfer(address sender, address recipient, uint256 amount) internal virtual {
        require(sender != address(0), 'ERC20: transfer from the zero address');
        require(recipient != address(0), 'ERC20: transfer to the zero address');

        _beforeTokenTransfer(sender, recipient, amount);

        _balances[sender] = _balances[sender].sub(amount, 'ERC20: transfer amount exceeds balance');
        _balances[recipient] = _balances[recipient].add(amount);
        emit Transfer(sender, recipient, amount);
    }
}
```

This ERC20 token contract allows users to transfer Ludus tokens. The contract starts with an initial supply minted to the contract owner. It includes the necessary functions from the ERC20 standard such as `transfer`, `transferFrom`, `approve`, `allowance`, `totalSupply`, and `balanceOf`. It also includes the necessary checks and internal transfers required by the ERC20 standard.

Note: This is a simplified version of an ERC20 token contract. Additional functionalities such as pausing, minting, and burning can be added based on the specific needs of the application.