# composer-samples
# Composer-Tuts

 1. create business network template
 
 ```
 yo hyperledger-composer:businessnetwork
 ```
 
 2. create archieve
 
 ```
composer archive create -t dir -n .
 ```
 3. Deploy business network archieve
 
 ```
 composer network install --card PeerAdmin@hlfv1 --archiveFile <bna archieve file name>
 ```
 
 4.start business network
 
 ```
 composer network start --networkName <business network name> --networkVersion 0.0.1 --networkAdmin admin --networkAdminEnrollSecret adminpw --card PeerAdmin@hlfv1 --file networkadmin.card
 
 ```
 5. Network card import&Ping Network
 
 ```
 composer card import --file networkadmin.card
 
 composer network ping --card admin@tutorial-network
 ```
 6. Generating Rest API
 
 ```
 composer-rest-server #serves at 3000
 ```
 7.Accessing via Playground
 
 ```
 composer-playground #serves at 8080
 ```
 
 8. Accesing via Web-App
 
 ```
 yo hyperledger-composer:angular
 ```
 Go to project and run  ```npm start``` to serve your web-app at 4200
