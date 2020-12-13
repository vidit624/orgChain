# OrganTracking

### Cloning the Repository
```sh
   git clone --recursive https://github.com/vidit624/orgChain
   cd orgChain/OrganTrackingBlockchainNetwork
```
##Steps to setup the network

1. Download Binaries
```sh
   https://drive.google.com/drive/folders/1HC5baB-KKz7_aGcSzb-UZUMZdeZvS1TA?usp=sharing
```
2. Generating Artficats
```sh
	./generateartifacts.sh
```
3. Start the netowrk  

```sh
  . setenv.sh 
  docker-compose up -d 
```

4. Build and join channel. Make sure that network is running 

```sh
   docker exec -it cli bash -e ./buildandjoinchannel.sh 
```

5. Install and intantiate the chain codes 
  
```sh
  docker exec -it cli bash -e  ./ctrack_install.sh
```

## Setting the APIs

```sh
	cd ../OrganTrackingApi
```

Starting The APIs

```sh
	./launchServices.sh
	docker-compose up -d
```

#### ========To destory  an existing APIs ( START)============= 
```sh
  ./stopServices.sh 
  docker-compose down 
```

#### ========To destory  an existing network ( START)============= 
```sh
  cd ../OrganTrackingBlockchainNetwork
  . setenv.sh 
  docker-compose down 
  ./removeImages.sh
  ./clearVols.sh
```