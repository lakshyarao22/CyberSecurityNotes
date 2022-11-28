# ArcSight 22.1

* **CDF**: Container Development Framework
* **Kubernetes**: Used to manage docker images

## Products
* Fusion
  * Soar
  * ArcSight Management Center
  * Fusion Dashboard
  * Reporting
  * Admin Capabilities are part of Fusion
  * TH and Database is not required on Fusion.
* Transformation HUB
* Intelligence (require TH and Database). 
* Recon (require TH and Database).
*  ESM 
   * We cannot access full capabilities of ESM from Fusion ESM, That's why we need Separate ESM.
*  Layered Analytics Identity Governance

> TH is Kafka in backend
> 
> ESM soon to be renamed to **detect**
## Connector
It can send logs in 3 languages
* CEF
* AVRO
* Binary


# Installation and Setup
  1. Access [SLD](https://sld.microfocus.com/) Portal
  2. MF Software Passport ID + SAID 
  3. put capabilities in images folder
  4. YAML in config folder 
  5. put metadata in its respective Folder.
  6. ./arcsight-install --cmd precheck
  7. ./arcsight-install --cmd prereq
  7. ./arcsight-install --cmd preinstall
  8. ./arcsight-install --cmd install (it will install CDF + Database)

                   AND/OR
     ./arcsight-install --cmd database (it will install only Database)

                   AND/OR
     ./arcsight-install --cmd cdf (it will install only CDF)

## R&D

/opt/installer/installers/cdf/install.property

make node large which have intelligence-namenode

# Important Command