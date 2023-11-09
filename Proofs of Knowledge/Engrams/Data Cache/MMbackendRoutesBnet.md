```javascript
import { Router } from "express";
import passport from "passport";
import refresh from "passport-oauth2-refresh";

const loginRouter = Router();

// configure Express
loginRouter.get('/battlenet',
  passport.authenticate('bnet'));



loginRouter.get('/battlenet/callback',
  passport.authenticate('bnet', { failureRedirect: '/' }),
  async function(req, res) {
    res.send(`
    <script>
      // Post user data to parent window
      window.opener.postMessage(${JSON.stringify(req.user)}, "*");
      
      // Close the current (pop-up) window
    </script>
  `)

  });


loginRouter.get("/refresh", async (req, res) => {
  passport.authenticate("bnet", { failureMessage: "Woopsie" });
  refresh.requestNewAccessToken('bnet', JSON.stringify(req.user.data.token), function(err, accessToken, refreshToken) {
    if (err) {
      console.error(err);
      res.status(500).json({ message: err.toString() });

    } else {  // The user is authenicated successfu
      res.status(200).json({ message: "Logged in", accessToken, refreshToken });
    }
  });
});


loginRouter.post("/logout", (req, res) => {
  passport.authenticate("bnet", { failureMessage: "Woopsie" });
  req.session.destroy(er => {
    if (er) {
      console.error(er);
      res.status(500).json({ message: er.toString() });
    } else {
      res.status(200).json({ message: "Logged out" });
    }
  });
});


loginRouter.use(function(err, res) {
  console.error(err);
  res.send("<h1>Internal Server Error</h1>", err);
  console.log(err);
});

export { loginRouter };

```