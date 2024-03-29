# OXIDANE

## WATER TRADING DAPP FOR PUBLIC


Oxidane is a decentralized application for water trading, it mainly
focuses on truck-based water delivery system. Oxidane eliminates the role of
middle man between Water-exchange and customers and makes the system
more transparent and trustable.

For more details Please read documentation file.

#  SETTING UP- START  :

**Step 1:** Download the repostory using the command:  
```
 git clone "https://gitlab.com/TeamKBA/ced_b4_projects/ced-b4-g01.git"
```
**Step 2:** Move to downloaded directory & Install the dependencies for testing using the command: 
```
 npm Install 
```
 **Step 3:** Move to frontend-react directory & Install the dependencies for Front-end using the command: 
```
 npm Install   
```
## Setting Up a Private-Chain(Ganache/Geth):

## Set up Ganache

**Step 1:** Activate Ganache on port 7545 with ChainID 5777  

or

## Set up Geth

**Step 1:** Move to Nodedata directory and open terminal and use command:
```
geth --identity "miner" --networkid 7877 --datadir data --nodiscover --mine --rpc --rpcport "8646" --unlock "0xf7d74504257947d965547ac3336c66cce68413a5" --ipcpath "~/.ethereum/geth.ipc" --rpccorsdomain "*" --rpcapi "db,miner,eth,net,web3,personal" --allow-insecure-unlock
```
**Password: vimal
```
copy Ipc path
```
**Step 2:** open terminal and use command:
```
geth attach <Ipc path> //paste copied ipc path
```
**Step 3:** Start mining using command:
 ```
 miner.start()
  ```   
## Test Smart Contract

Using truffle developement
**Step1:** Move to downloaded directory,open terminal and use command
 ```
 truffle develop
 ```
 ```
 test 
  ```
Using ganache

**Step1:** Run ganache

**Step2:** Move to downloaded directory,open terminal and use command
```
truffle test
```
## Deploy Smart Contract on Private/Public network:

## To deploy on ganache 

**Step 1:** open terminal and use command:
```
truffle migrate
```
## To deploy on geth 

**Step 1:** open terminal and use command:
```
truffle migrate --network geth_private
```
## To deploy on Ropsten

**Step 1:** open terminal and use command:
```
truffle migrate --network ropsten_infura
```

## Starting Dapp

**Step 1:** Move to frontend-react drectory,open terminal and use command:
```
npm start
```
**Step 2:** Choose desired network in metamask
```
If using Geth then use localhost 8646 with chainId 7877
```
```
If using ganache then use localhost 7545 with chainId 5777
```

## Setting up accounts

## In ganache

**Step 1:** Setup Admin Account
```
copy contract deployer private key from ganache and import account as Admin in metamask
```
**Step 2:** Setup Water-Exchange Account
```
create Water-Exchange account in metamask by importing private key of an account from ganache
```
**Step 3:** Setup Customer Account
```
create customer account in metamask by importing private key of an account from ganache
```

## In Geth
**Step 1:** Setup Admin Account
```
import Admin account by using private key=54897ed568fa7226c320e8db70c2f2ced0d6a2a36118d78508ae3920ad26b2a7

```
**Step 2:** Setup Water-Exchange  Account
```
import Water-Exchange account by using private key=f086385030b9f3e0335ddded71a5d914f4ca9a38d5b5e97e80a725ade901f76c

```
**Step 3:** Setup Customer Account
```
import Customer account by using private key=cae456935e04c1d8a69ec93c1dec95ee27d4b629e117daad70b7e0d7bccbbd4d

```
## In Ropsten
**Step 1:** Setup Admin Account
```
Private key of deployer is provided inside the Ropsten Directory use it to setup Admin acount
should have some Ether for transactions 
```
**Step 2:** Setup Customer Account
```
Create an account in metamask
should have some Ether for transactions 
```
**Step 3:** Setup Water-Exchange Account
```
Create an account in metamask
should have some Ether for transactions 
```

# SETTING UP- END 

# WORKFLOW - START

## Note-:
***1** After each account change reload the page otherwise it may cause Rpc errors

***2** Avoid white spaces while copying and pasting account address

**Step 1:** REGISTERING WATER EXCHANGE
```
1.Select Admin account and and make sure it is connected
2.Go http://localhost:3000/admin or Admin on navbar, Provide exchange registration details and click submit
3.give water exchange account address for exchange address field

eg:
Exchange Address:0x4E35E79b19EDF952FA204940Ec6893861015ac36
Location:tvm
cluster:South kerala
Select APPROVAL CERTIFICATE FILE:file
```
**Step 2:** UPDATE WATER QUANTITY & DELIVERY CHARGE IN WATER EXCHANGE
```
1.Select Water-Exchange account and and make sure it is connected
2.Go http://localhost:3000/exchangesignup or Exchange on navbar, Provide waterexchange water updation details and click add water.
3.provide delivery charge and click update
eg:Select Water Type:Drinking
Amount to Increment(in kl ):100
Update Delivery charge:2 OXD
```
**Step 3:** Signup as customer
```
1.Select Customer account and and make sure it is connected
2.Go http://localhost:3000/signup or click User on navbar, Provide user category and click register
```
**Step 4:** Buytokens as customer
```
Provide token quantity in Buytoken form and click submit 
eg:Token Amount:2
```
**Step 5:** Buywater as customer
```
1.select water exchange to purchase by selecting cluster in AVAILABLE WATER EXCHANGES
2.copy exchange address from the exchange list
3.Paste to Exchange Address field in Buy Water form
4.provide details for purchase
eg:
Exchange Address:0xc839f437752f95a86ed2f8DDb27843DfFAF377ea
WaterType:Drinking
Water Quantity(kl):2
Delivery Cluster:South kerala
Delivery Location:tvm
contact no:1234567789
```
**Step 6:** Trigger Delivery as Water-Exchange
```
1.Select Water-Exchange account and and make sure it is connected
2.Go http://localhost:3000/exchangesignup or click Exchange on navbar
3.click deliver button on DELIVERY PENDING LIST
```
**Step 7:** Trigger Delivery confirmation as Customer
```
1.Select Customer account and and make sure it is connected
2.Go http://localhost:3000/user or click User on navbar
3.click Received button on DELIVERED LIST
```
**Step 8:** Selltokens as Water-Exchange
```
1.Select water-exchange account and and make sure it is connected
2.Go http://localhost:3000/exchangesignup or click Exchange on navbar
3.Enter the quantity to sell in sellTokens form

```
**Step 9:** To Reject delivery as Customer
```
Repeat Steps from step 4 to 6
1.Select Customer account and and make sure it is connected
2.Go http://localhost:3000/user or click User on navbar
3.Enter details in Reject form and click submit

eg:
Exchange Address:0xc839f437752f95a86ed2f8DDb27843DfFAF377ea
Purchase no:1
```



#   WORKFLOW - END 
