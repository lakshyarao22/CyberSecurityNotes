# Connector

## Notes

* Earlier ESM Supported Binary logs but now ista depreciated.

* Only users Which have kafka management role can access the same.

[Cmak Kafka](https://github.com/yahoo/CMAK)

## Reduce EPS

* Regex Filtering
* Aggregation
* Smart Connector Normalizing Filter

## Import Certificates on connector

``` bash
hostname  ## master.advantageinc.org
cd /opt/arcsight/kubernetes/scripts/
./cdf-updateRE.sh ## Certificate is generated
## Copy Certificate and save as .crt file
                OR
./cdf-updateRE.sh > /opt/master1.crt
```
Backup following file

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
