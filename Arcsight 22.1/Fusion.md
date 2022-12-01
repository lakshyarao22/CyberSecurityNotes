# Fusion

To Install Bare Minimum fusion we need fusion and NFS.

To Install fusion only with 3 workers and 1 master we need following yaml file

```yaml
cluster:
  default-node-size: medium
  master-api-ssl-port: 7443
  allow-worker-on-master: false
  enable-fips: false
  master-nodes:
    - hostname: master.advantageinc.org
      username: root
  worker-nodes:
   - hostname: worker1.advantageinc.org
     username: root
     labels: [fusion]
   - hostname: worker2.advantageinc.org
     username: root
     labels: [fusion]
   - hostname: worker3.advantageinc.org
     username: root
     labels: [fusion]

suite:
  products: [fusion]
  config-params:
    arcmc-generator-id-start: 100
    arcmc-generator-id-end: 1000
    arcmc-generator-id-enable: true
    recon-enable: true

nfs:
  node:
    hostname: nfs.advantageinc.org
    username: root
  type: new
  root-folder: /opt/arcsight-nfs
  uid: 1999
  gid: 1999
```

* If NFS parameters are not mentioned than precheck command will automatically install NFS on master node.

## ESM To Fusion SOAR Log Forward Connector

* Follow Previous steps
* Select CEF Syslog format
* Select host master.advantageinc.org:**32200**
* Enable *ArcSightListenerEnabled* on https://master.advantageinc.org/soar/#/configuration/parameter
* Change following Parameters on Installer

``` yaml
Ip/Host: master.advantageinc.org
Port: 32200
Protocol: Raw TCP
Forwarder: false
CEF Version: 0.1
```

* If Facing Error try changing password for apiSOAR user or Disable or enable the user
