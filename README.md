# Hyperledger_M1_Templet
this is a build of Hyperledger Fabric 2.2 templet for apple M1 as binaries are not natively available 

--> Change to the Fabric repo
  cd $GOPATH/src/github.com/hyperledger/fabric
  
--> Build the Fabric binaries
  make native

--> Copy the binaries to the Fabric-Samples repo
  mv build/bin $GOPATH/src/github.com/hyperledger/fabric-samples

--> Copy sampleconfig directory to Fabric-Samples and rename to "config'
  mv sampleconfig $GOPATH/src/github.com/hyperledger/fabric-samples/config

--> Change to the Fabric-CA repo
  cd $GOPATH/src/github.com/hyperledger/fabric-ca

--> Build the Fabric-CA-Client binary
  make fabric-ca-client

--> Copy the Fabric-CA-Client binary to the Fabric-Samples `bin` directory
  mv bin/fabric-ca-client $GOPATH/src/github.com/hyperledger/fabric-samples/bin

--> That's all, you can now change back into Fabric-Samples and run the test-network
  cd $GOPATH/src/github.com/hyperledger/fabric-samples/test-network
