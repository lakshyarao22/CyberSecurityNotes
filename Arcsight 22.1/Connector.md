# Connector

## Notes

* Earlier ESM Supported Binary logs but now ista depreciated.

* Only users Which have kafka management role can access the same.

Open Source Repo for [Cmak Kafka](https://github.com/yahoo/CMAK)

## Reduce EPS

* Regex Filtering
* Aggregation
* Smart Connector Normalizing Filter

## Connector for CEF Output

* Connector is used to output CEF Format to TH.
* kafka Topic should be **"th-cef"**
* Kafka Broker is synonemous to Worker so address should be workers hostname i.e.

* Require Acknowldge from all is good for reliability but very heavy on performance

``` bash
worker1.advantageinc.org:9092,worker2.advantageinc.org:9092,worker3.advantageinc.org:9092
```

* As we are not using the SSL in CEF no need to import SSL Certificate

* Pasting Replay Files will export test logs to FUSION

## Import Certificates on connector

Certificate is used for encryption on logs from event source to ESM

``` bash
hostname  ## master.advantageinc.org
cd /opt/arcsight/kubernetes/scripts/
./cdf-updateRE.sh ## Certificate is generated
## Copy Certificate and save as .crt file
                OR
./cdf-updateRE.sh > /opt/master1.crt # Generate Certificate and paste it into master1.crt
```
Backup certificate  file

``` powershell 
C:\arcsight\SmartConnector\th-AVRO\current\jre\lib\security\cacerts ## Backup this File

.\arcsight.bat keytoolgui ## run in powershell as Administrator
```

1. open Keytool gui.
2. open Keystore (cacert).
3. Go to tools and import trusted Certificate.
4. Import master1.crt.
5. save the keystore.

run arcsight agent

```powershell
.\arcsight agents
```

## Connector for AVRO

* All the steps same as CEF but here we will import certificate as we are using SSL on AVRO connector.

* Now use **th-arcsight-avro** as Kafka Topic and use **AVRO** as content type.

* In schema registry paste hostname of machine on which certificate was generated and also the ssl port i.e.

``` note
master.advantageinc.org:32081
```

* In SSL TrustStore filepath give path of cacerts

``` powershell
C:\arcsight\smartConnector\th-AVRO\current\jre\lib\security\cacerts
```

* As mentioned use truststore Passkey on password field.

### Agent.properties

* Enable inheretance for agent.properties.

## Importing Connectors to ArcMC

* Just go to node management
* Go to Default location or location you want your connector to add
* Add Windows or connector hostname
* Select Type as software Connector
* use port 9001,9002
* Give Credentials and import Cretificates.
* Finally Click **ADD**

---
Note:- Connectors should be running on host machine.