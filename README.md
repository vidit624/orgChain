# OrganTracking
orgChain seeks to address challenges faced by organisations(hospitals and nurseries)  in maintaining the security of donated organs information.It is designed to provide instant help and support to people in need of organs through a legalised channel without the involvement of any third party.To take into consideration the privacy of organisations and maintain the trust of public,the various features provided in our system are :
All legally authorised organisations can be inserted into the public channel of the blockchain
No third party can enter into the chain without the permission of all members already present in the chain
Any member of the public chain can create blocks regarding all available donated organs present
Any member  of the public channel can access the already available organ information in the chain and can track the member who added that block in the chain.In this way,it can directly contact the other organisation if needed and can get the organ transported without involving any third party hindrance.
To keep the donor’s information secure,each organisation is provided with a private channel that can be accessed only by it.  

# Pre-requisites
- Golang
- Hyperledger framework
- Docker 
- CouchDB
- Swagger 
- HTML
- CSS 
- Javascript

# Setting up the project
Follow the instructions below to set up the blockchain project in your system:

### Cloning the Repository
```
$git clone --recursive https://github.com/vidit624/orgChain
$cd orgChain/OrganTrackingBlockchainNetwork

```
### Steps to setup the network

1. Download Binaries
```
$https://drive.google.com/drive/folders/1HC5baB-KKz7_aGcSzb-UZUMZdeZvS1TA?usp=sharing

```
2. Generating Artficats
```
$./generateartifacts.sh

```
3. Start the netowrk  

```
 $. setenv.sh 
 $docker-compose up -d 

```

4. Build and join channel. Make sure that network is running 

```
$docker exec -it cli bash -e ./buildandjoinchannel.sh 

```

5. Install and intantiate the chain codes 
  
```
$docker exec -it cli bash -e  ./ctrack_install.sh

```

### Setting the APIs

```
$cd ../OrganTrackingApi
```

#### Starting The APIs

```
$./launchServices.sh
$docker-compose up -d

```

#### ========To destory  an existing APIs ( START)============= 
```
$./stopServices.sh 
$docker-compose down 
```

#### ========To destory  an existing network ( START)============= 
```
$cd ../OrganTrackingBlockchainNetwork
$. setenv.sh 
$docker-compose down 
$./removeImages.sh
$./clearVols.sh
```

# Demo of the project
Demo of the project can be viewed using the [youtube link](https://www.youtube.com/watch?v=ErZcke-5G0A&feature=youtu.be)
