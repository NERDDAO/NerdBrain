```javascript
import passport from 'passport';
import express, { Router } from 'express';
import path from 'path';
import { MongoClient } from 'mongodb'
import { fileURLToPath } from 'url';
import https from 'https';
import xml2js from 'xml2js';
const __filename = fileURLToPath(import.meta.url);

const __dirname = path.dirname(__filename);
const url = 'mongodb://127.0.0.1:27017';
const client = new MongoClient(url);
await client.connect();
console.log('Connected successfully to server');
// Database Name
const dbName = 'myProject';
const dbRouter = Router();

const useRegex = (input) => {
  let regex = /"displayid":(?<displayid>[0-9]+)/i;
  input = input.match(regex);
  let displayid = input?.groups.displayid;
  return displayid;
}  //let response = result.wowhead.item[0].json[0];
dbRouter.use(express.static(path.join(__dirname, "../../dist/")));
console.log(__dirname);



dbRouter.get('/database', async (res) => {
  // Use connect method to connect to the server
  const db = client.db(dbName); // Connect to the Database
  const collection = db.collection('1playerCollection2323333'); // Access to 'players' collection
  // Access to 'players' collection
  const itemCollection = db.collection('itemCollection2334'); // 


  const items = await itemCollection.find({}).toArray();
  const players = await collection.find({}).toArray();

  // Get all players from collection
  res.json({ items: items, players: players }); // Response to MongoClient
});


dbRouter.post('/db', async (req, res) => {
  // Write the generated HTML to the document body
  passport.authenticate('bnet', { failureMessage: 'Woopsie' });
  // Parse JSON body
  const player = await req.body;



  const db = client.db(dbName); // Connect to the database
  const collection = db.collection('1playerCollection2323333');
  const itemCollection = db.collection('itemCollection2334'); // 

  itemCollection.createIndex({ ItemId: 1 }, { unique: true })
  collection.createIndex({ id: 1 }, { unique: true })





  if (!player.equipped_items) {
    try {
      let index = await collection.findOne({ id: player.id });

      console.log(index, player)
      if (index === null && player !== null) {
        collection.insertOne(player); // inser
        console.log('inserted' + player)
      }



    } catch (err) {

      console.log(err.message)
    }
    let promiseArray = [];
    await player?.equipped_items.map(async (item) => {

      let itemUrl = `https://www.wowhead.com/item=${item.item.id}&xml`
      var parser = new xml2js.Parser();
      let data = '';


      promiseArray.push(new Promise(async (resolve) => {
        https.get(itemUrl, function(res) {
          try {
            if (res.statusCode >= 200 && res.statusCode < 400) {
              res.on('data', function(data_) {
                data += data_.toString();

              });
              res.on('end', function() {

                parser.parseString(data, async function(err, result) {
                  let dispid = result.wowhead.item[0].json[0];

                  let response = await useRegex(dispid)


                  console.log(response)
                  if (response === undefined) return;
                  let index = await itemCollection.findOne({ ItemId: item.item.id });
                  console.log(index)
                  try {

                    if (index === null && response !== null) {
                      itemCollection.insertOne({ ItemId: item.item.id, displayId: response })
                      console.log('inserted' + item.item.id + ' ' + response + ' ' + item)
                    }





                  } catch (err) {

                    console.log(err.message)
                  }




                });




              })
              resolve(body)

            }

          } catch (e) {
            parser.on('error', function(err) { console.log('Parser error', err); });
          }


        })


      })
      );
    })
    await Promise.all(promiseArray)
    res.json({ status: 'success', message: 'Players added to DB', body: promiseArray });
  }


})



dbRouter.get('/render', (req, res) => {
  const { characterId: player, name, gender, race, facial_hair, HEAD, SHOULDERS, CHEST, WAIST, LEGS, FEET, WRIST, HANDS, BACK, MAIN_HAND, OFF_HAND } = req.query;
  // fetch displayID library 
  // match itemID -> get DisplayID Eg: {15304: 10013 }
  // 
  //
  console.log("rendering")
  res.render('./renderer/test.ejs', { title: player, counter: Number(race), name: name, gender: gender, facial_hair: facial_hair });
  /*  const itemCollection = db.collection('itemCollection23'); // 
  const db = client.db(dbName); // Connect to the database

    let inventory = {
    HEAD: HEAD ? HEAD : null,
    SHOULDERS: SHOULDERS ? SHOULDERS : null,
    CHEST: CHEST ? CHEST : null,
    WAIST: WAIST ? WAIST : null,
    LEGS: LEGS ? LEGS : null,
    FEET: FEET ? FEET : null,
    WRIST: WRIST ? WRIST : null,
    HANDS: HANDS ? HANDS : null,
    BACK: BACK ? BACK : null,
    MAIN_HAND: MAIN_HAND ? MAIN_HAND : null,
    OFF_HAND: OFF_HAND ? OFF_HAND : null,
  };
  let promiseArray = [];
  try {
    promiseArray.push(new Promise(async (resolve, reject) => {
      for (const [key, value] of Object.entries(inventory)) {
        itemCollection.findOne({ ItemId: value }, (err, result) => {

          inventory[key] = result.displayId;

          console.log(inventory, 'inventory')




        })
      }
      resolve(inventory)
    }));

    await Promise.all(promiseArray).then(async (values) => {
      console.log(values, 'values')



    })
  } catch (err) {
    console.log(err)
  }*/

})


export { dbRouter };



```