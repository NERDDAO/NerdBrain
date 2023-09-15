Hey it's random code here and today I want to showcase how to create a mongodb instance inside a dragon container I would then go in through this Docker container and show you some basic mongodp commands which allow us to insert into some Json Dove extract pyramid and so on so which is very simply here you have a very very simple Docker file which mainly contains of prom which 

 Extracts a mango image from darker Hub in this case I didn't add any text so it's just going to be the latest and very simple setup in a more real case I would probably add a specific version we then don't in this case have any environment variables which could be set to Define some passwords for instance but we're just going to keep it simple and just want to showcase that by default exposes Port 270 and 17. so in a 

 Real setup where I would actually like to connect to our database reduce this port so now to actually start a dark container I am inside my terminal at the same position of my data file as you can see here which then allows me to very simply blogger built and we'll give it a tag let's call it and we're going to be building it from our current position which is 

 Connected to our Docker file for me it's going to be very fast because I think it might already be cached because already tried doing this a few times but we can then do Docker images which now have a Repository to then run this image it would send me to docker run mango and it's then going to be printing a few setup informations to the screen I would then very simply go into a 

 Second terminal where we would first check taxes working and that this container is running so let's do WPS now see we have a container running with an ID a few seconds ago and as we Define it's exposing this port this isn't going to be used but we now have this running container and I wouldn't like to actually interact with the container to Showcase it works and to Showcase we actually have a 

 Instance running so we'll do mango oh not docker exec Dash interact mode then our container ID and we can then Define which files we will run from our container in this case which allow us to get a pass terminal running inside our container so I can now do from us to see where inside the container we have some basic 

 Setup with some Dev files from home and a bunch of other stuff but most interestingly now if we do mango sh would get a mango shell and note a newer version of we're going to be using sh in all the versions it's just gonna be so the mango shell it's a newer thing added in the later versions of mango because we're just using it's going to be the newest version so we need to use mango sh 

 So we now is inside the mongodb instance and I could then see here that right now we are pointing to a test database which I actually know doesn't contain anything so we could do show collections because in mongodb we have a hierarchy of databases which contains collections which is then going to be containing Json information so our test which is where we're putting 

 Right now actually doesn't contain any information but test doesn't even contains or exist either so it will show DPS show all databases we can say information so we have admin config and logo and it's actually kind of interesting is that we only have things existing that contains information but if I try to insert the into test 

 It's going to be created so let's actually first just take a look at something that already exists so I would use admin for example so we switch to TP admin again then once again do show Collections and internet admin will have a system.version collection we could then do exactly showcase what's in here we could do DB which is going to be pointing to our current database in this case admin 

 DP Dot system dot version dot find and note that find is actually a function we're calling on this instance and this one is actually empty so that one is actually kind of boring let's write another one let's try use logo show collections we have a startup lock we can then do DB that start uh block Dot find 

 And here we actually get a bunch of creation information and if we didn't want it to create a new database and insert some information we could use test once again so use test still node the test doesn't exist but let me showcase when we insert into test it's going to be created so we have not connected to our testdb let's now insert something into test so refers to DB pointing a test we then create a new 

 Collection inside test called people and note once again people have not already created but when we in search of the ends of people that's going to be created so DB the people third insert and we're going to inserting something that's Json and let's just do very simple persons so let's do the name Hans he's gonna be a bit older as to H 

 50 . and let's do an email as well off runs at email Dot dot com foreign we want to insert defining well if we just inserting one in this case one person or one entry or multiple but it has been acknowledged and we created and got an ID for this insert so we can now do 

 Show DBS showcase you already have I also have a test database but if we now do DB dot people Dot fine we can now see that we have our Json object containing our name our age and our email and we should also note that we know an object ID which was returned when we created our hands or Hans J object which could be useful and some real application where we 

 Insert something to a database we then get an ID returned which could then be used to update or change if you want to keep manipulating this object but just very simply we use insert probably should use insert one so let me X just do it again to Showcase that now we just simply continue doing DB the people that insert and if we should actually try being a better person using them actually not 

 Deprecated functionality we do just insert and so one and instead of just doing hands video hunts two and there we go it has now been inserted and we got an orbit ID once again has returned and if we now do db.people.find we can now see that we have two objects inside our DB people collection 

 And node that actually works a bit different from here like normal SQL that we haven't defined anything it's just data which also allows that we could actually insert and two once again and we would now actually have two people with the exact same name exact same age and like exact same email but mango doesn't care because they are creating their own object IDs which is going to be different each time but that 

 Is the basic Showcase of a once showcase today in this video I will probably create multiple videos in the future actually showcasing how we can connect different applications to this in this inner container to actually use it in a more real scenario so if you enjoyed this quick showcase please leave a like And subscribe and I wish you a wonderful day 