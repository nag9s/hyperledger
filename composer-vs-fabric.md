[https://stackoverflow.com/questions/45505333/difference-between-hyperledger-composer-and-hyperledger-fabric](https://stackoverflow.com/questions/45505333/difference-between-hyperledger-composer-and-hyperledger-fabric)

Hyperledger Composer simplifies application development on top of the Hyperledger Fabric blockchain infrastructure.

If you are interested in the blockchain infrastructure, start with the Fabric[tutorials](https://hyperledger-fabric.readthedocs.io/en/latest/build_network.html#).

If you are interested in blockchain applications, start with the Composer[tutorials](https://hyperledger.github.io/composer/latest/tutorials/tutorials.html).

The Fabric tutorials also include samples of low level chaincode development \(in golang\). Composer is a higher level application development framework.

I'd suggest trying both to get an overall view of the capabilities.

As a Java developer, you will also want to check out the[Fabric Java SDK](https://hyperledger-fabric.readthedocs.io/en/latest/fabric-sdks.html)for building Java client applications that interact with the blockchain. There is also Java chaincode capability under construction, but not yet available in 1.0.0.





Does Composer generate the go language smart contracts depending on the business network and deploy them in the docker ? Or is it using a generic Smart contract for all the business networks ? I saw a video in Youtube, which mentioned generic chaincode, and was confused. – Ashishkel Aug 9 '17 at 9:47

1

Composer itself runs as a smart contract on Fabric. – neuromouse Aug 10 '17 at 14:28

1

Composer does not directly generate chaincode or 'Go'. It uses a generic chaincode that maps composer models to chaincode tables and runs transaction processor functions in the javascript interpreter in a javascript engine. So it runs in its own runtime environment and chaincode container. Each composer business network \(ie with the smart contract logic, written in javascript and created as part of the business network\) is deployed to it's own Chaincode container. –

