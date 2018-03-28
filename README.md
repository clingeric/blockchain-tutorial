# Blockchain For Business Tutorial


## Step 1. Import the car auction sample
1. Open a web browser and go to http://composer-playground.mybluemix.net. Dismiss the welcome
screen to show the playground wallet screen which is used to connect and deploy new business
networks:

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/1.PNG)

2. Click the “Deploy a business network” box. Then scroll down and select the carauction-network:

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/2.PNG)

3. Next give the business network a name and description:

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/3.PNG)

4. Click the Deploy button to deploy the new car auction business network:

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/4.PNG)

5. Click “Connect now” in the new identity card for the carauction network:

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/5.PNG)

6. Take a minute to read through the description of the car auction sample, to help understand the
participants, assets and transactions associated with this particular network.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/6.PNG)

## Step 2. Adding Participants
In the next section we will now work with the deployed car auction blockchain network.

We will first instantiate three Member participants of the car auction business network:

* Alice Smith (alice@email.com), who will make a bid on a car,
* Bob Jones (bob@email.com), who will also make a bid on a car, and
* Charlie Brown (charlie@email.com), who currently owns a car.

1. Click the **Test** tab and then click on the Member participant registry:

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/7.PNG)

The registry is empty as no members have currently been defined.

2. Click on **Member** to view there are no current members in the environement

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/8.PNG)

3. Click **Create New Participant** to add a new Member.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/9.PNG)

4. Type the correct values into the JSON data structure to add Alice to the business network. Let’s give her a starting balance of `10000`.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/10.PNG)

5. Click **Create New** to add Alice to the registry.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/11.PNG)

6. Do the same for Bob. Let’s give him a starting balance of `5000`.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/12.PNG)

7. Finally do the same for Charlie. He hasn’t got so much money (he’s selling his car, after all) so let’s give him a starting balance of `100`.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/14.PNG)

8. Verify that all participants in the business network have been correctly defined. Use the appropriate Edit button (![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/16.PNG)) to make any changes.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/17.PNG)

## Step 3: Adding a Vehicle

We will now add Charlie’s car to the Vehicle Asset registry.

1. Click the **Vehicle** asset registry.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/18.PNG)

2. This registry contains no assets currently. Click **Create New Asset** to add a new asset.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/19.PNG)

3. Instantiate the car by adding a vehicle identification number (VIN) of `1234` and assign it to Charlie by adding to the JSON object as follows. (We use his email address to identify him; this was specified as the key field in the User definition by using the `identified by` statement.)

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/20.PNG)

4. Click Create New to add the new vehicle to the registry.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/21.PNG)

5. View your newly added asset in the registry.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/22.PNG)

## Step 4: Putting Vehicle up for Sale

Next, we will put the car up for sale by creating a `VehicleListing` instance.

1. Click the **VehicleListing** asset registry. Again, the VehicleListing registry should be empty.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/23.PNG)

2. Click **Create New Asset** to add the asset.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/24.PNG)

3. Update the fields and remove the random offers. Syntactic validation of the object occurs at this
point, so correct any errors if necessary.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/25.PNG)

4. Click **Create New** to add the new vehicle listing to the registry.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/26.PNG)

5. View the listing in the registry.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/27.PNG)

## Step 5: Accept Bids for the Vehicle

We will now let Alice and Bob bid on the vehicle.

1. Click **Submit Transaction**.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/28.PNG)

2. Let Alice put in a bid of `6000`.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/29.PNG)

3. Click **Submit** to submit the offer transaction.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/30.PNG)

You can see that the transaction was successful in the Historian registry.

4. Switch to view all transactions by clicking **All Transactions**.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/31.PNG)

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/32.PNG)

You can view the additional transactions for creating participants and assets. Click view data for more information.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/33.PNG)

5. Let Bob put in a bid of `4000`.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/34.PNG)

6. Verify the transactions in the registry.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/35.PNG)

Note that the transactions cannot be edited or individually deleted after they are submitted; this is one of the defining characteristics of a blockchain.

## Step 6: Close the Bid

Now we want to close the bidding on the listing. To do so, we need to submit a CloseBidding transaction.

1. Submit a new transaction. From the Transaction Type menu, select CloseBidding.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/36.PNG)

2. Click Submit to submit the CloseBidding transaction.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/30.PNG)

3. Verify that the transaction has been added to the blockchain transaction registry. Click view data to see the content of the transaction.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/37.PNG)

Based on the bids that were submitted, Alice should now be the owner because she put in the highest bid. We should also be able to verify that the owner of the car has changed, and specific balances increased or decreased accordingly.

4. Go to the Vehicle asset registry to see that the vehicle owner has been updated to Alice.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/38.PNG)

5. Note that the vehicle listing now shows the car as sold.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/39.PNG)

6. Go to the Member asset registry to see that Charlie’s balance has increased by the winning bid amount, and that Alice’s balance has decreased by the same.

![alt text](https://github.com/clingeric/blockchain-tutorial/blob/master/img/40.PNG)

**Congratulations!** You have successfully transferred assets in a blockchain.

![alt text](https://media.giphy.com/media/111ebonMs90YLu/giphy.gif)


