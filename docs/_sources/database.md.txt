# Cloudmesh Database

Cloudmesh has a database in whic a local copy of information about objects that
are stored in the cloud is maintained. The objects contain all information of
the cloud that can be retrieved with the raw provider but are enhanced with a
cloudmesh attribute dict. Potential security related attributes, will hoever be removed from it so they are not stored in the database.


This dict looks like

```
"cm": {
   "kind": the kind of the provider
   "cloud": the cloud or service name, will be renamed to service in future)
   "name": a unique name of the object
}
```

We list in the next section examples of such data objects

## Virtual Machines


### Openstack

The compute provider kind is `openstack`. The Provider is located at 

* <https://github.com/cloudmesh/cloudmesh-cloud/blob/master/cloudmesh/compute/virtualbox/Provider.py>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-cloud/blob/master/cloudmesh/compute/vm/Provider.py>

#### Flavor

```
{
    "_id" : ObjectId("5ca798a7dc64f18b19e644e1"),
    "id" : "1",
    "name" : "m1.tiny",
    "ram" : 512,
    "disk" : 1,
    "bandwidth" : null,
    "price" : 0.0,
    "extra" : {},
    "vcpus" : 1,
    "ephemeral_disk" : 0,
    "swap" : "",
    "cm" : {
        "kind" : "flavor",
        "driver" : "openstack",
        "cloud" : "chameleon",
        "created" : "2019-04-05 18:04:23.621043",
        "name" : "m1.tiny",
        "collection" : "chameleon-flavor",
        "modified" : "2019-04-06 06:50:23.894035"
    },
    "updated" : "2019-04-06 06:50:23.867695"
}
```

#### Image

```
{
    "_id" : ObjectId("5ca798abdc64f18b19e644e9"),
    "id" : "4c8e6dac-97f0-4224-b7a2-0daef96b5c9f",
    "name" : "CC-Ubuntu16.04",
    "extra" : {
        "visibility" : null,
        "updated" : "2019-03-25T21:21:06Z",
        "created" : "2019-03-25T21:20:51Z",
        "status" : "ACTIVE",
        "progress" : 100,
        "metadata" : {
            "build-repo-commit" : "4ba0beb418de52f0d3bf93a94392b662d653c073",
            "build-variant" : "base",
            "build-os-base-image-revision" : "20190325",
            "build-os" : "ubuntu-xenial",
            "build-tag" : "jenkins-cc-ubuntu16.04-builder-34",
            "build-repo" : "https://github.com/ChameleonCloud/CC-Ubuntu16.04"
        },
        "os_type" : null,
        "serverId" : null,
        "minDisk" : 0,
        "minRam" : 0
    },
    "cm" : {
        "kind" : "image",
        "driver" : "openstack",
        "cloud" : "chameleon",
        "created" : "2019-04-05 18:04:27.417958",
        "updated" : "2019-03-25T21:21:06Z",
        "name" : "CC-Ubuntu16.04",
        "collection" : "chameleon-image",
        "modified" : "2019-04-06 06:50:33.747656"
    }
}

```

#### VM

```
{
    "_id" : ObjectId("5ca798acdc64f18b19e6454e"),
    "id" : "f531d2df-c472-4b32-8239-0e3969d33ebb",
    "name" : "exp-grp-gregor-vm-1",
    "state" : "running",
    "public_ips" : [],
    "private_ips" : [
        "192.168.0.249"
    ],
    "size" : null,
    "created_at" : ISODate("2019-04-01T11:05:56.000-04:00"),
    "image" : null,
    "extra" : {
        "addresses" : {
            "CH-819337-net" : [
                {
                    "OS-EXT-IPS-MAC:mac_addr" : "fa:16:3e:9d:ca:c2",
                    "version" : 4,
                    "addr" : "192.168.0.249",
                    "OS-EXT-IPS:type" : "fixed"
                }
            ]
        },
        "hostId" : "64472a496451a2d599c215a8e86275191c9e3fb9d53790de35bbb6dc",
        "access_ip" : "",
        "access_ipv6" : "",
        "tenantId" : "CH-819337",
        "userId" : "tg455498",
        "imageId" : "4c8e6dac-97f0-4224-b7a2-0daef96b5c9f",
        "flavorId" : "3",
        "uri" : "http://openstack.tacc.chameleoncloud.org:8774/v2/CH-819337/servers/f531d2df-c472-4b32-8239-0e3969d33ebb",
        "service_name" : "nova",
        "metadata" : {},
        "password" : null,
        "created" : "2019-04-01T15:05:56Z",
        "updated" : "2019-04-01T15:06:06Z",
        "key_name" : "gregor",
        "disk_config" : "MANUAL",
        "config_drive" : "",
        "availability_zone" : "nova",
        "volumes_attached" : [],
        "task_state" : null,
        "vm_state" : "active",
        "power_state" : 1,
        "progress" : 0,
        "fault" : null
    },
    "cm" : {
        "kind" : "node",
        "driver" : "openstack",
        "cloud" : "chameleon",
        "updated" : "2019-04-06 06:50:35.592158",
        "name" : "exp-grp-gregor-vm-1",
        "created" : "2019-04-05 18:04:28.376784",
        "collection" : "chameleon-node",
        "modified" : "2019-04-06 06:50:35.596479"
    }
}

```

## Azure AzProvider


The compute provider kind is `azure`. The Provider is located at 

* <https://github.com/cloudmesh/cloudmesh-cloud/blob/master/cloudmesh/compute/virtualbox/Provider.py>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-cloud/blob/master/cloudmesh/compute/azure/AzProvider.py>

### Flavor

### Image

### VM


```
{
    "_id" : ObjectId("5cbe0513b6ac5a154ef64a26"),
    "additionalCapabilities" : null,
    "availabilitySet" : null,
    "diagnosticsProfile" : null,
    "hardwareProfile" : {
        "vmSize" : "Standard_DS1_v2"
    },
    "id" : null,
    "identity" : null,
    "instanceView" : null,
    "licenseType" : null,
    "location" : "eastus",
    "name" : "testvm1",
    "networkProfile" : {
        "networkInterfaces" : [ 
            {
                "id" : null,
                "primary" : null,
                "resourceGroup" : "test"
            }
        ]
    },
    "osProfile" : {
        "adminPassword" : null,
        "adminUsername" : "ubuntu",
        "allowExtensionOperations" : true,
        "computerName" : "testvm1",
        "customData" : null,
        "linuxConfiguration" : {
            "disablePasswordAuthentication" : true,
            "provisionVmAgent" : true,
            "ssh" : {
                "publicKeys" : [ 
                    {
                        "keyData" : "ssh-rsa ...."
                        "path" : "/home/ubuntu/.ssh/authorized_keys"
                    }
                ]
            }
        },
        "requireGuestProvisionSignal" : true,
        "secrets" : [],
        "windowsConfiguration" : null
    },
    "plan" : null,
    "provisioningState" : "Succeeded",
    "resourceGroup" : "test",
    "resources" : null,
    "storageProfile" : {
        "dataDisks" : [],
        "imageReference" : {
            "id" : null,
            "offer" : "UbuntuServer",
            "publisher" : "Canonical",
            "sku" : "18.04-LTS",
            "version" : "latest"
        },
        "osDisk" : {
            "caching" : "ReadWrite",
            "createOption" : "FromImage",
            "diffDiskSettings" : null,
            "diskSizeGb" : null,
            "encryptionSettings" : null,
            "image" : null,
            "managedDisk" : {
                "id" : null,
                "resourceGroup" : "test",
                "storageAccountType" : null
            },
            "name" : "testvm1_OsDisk_1_a6a6a6a7639468d88e7b018385e225f",
            "osType" : "Linux",
            "vhd" : null,
            "writeAcceleratorEnabled" : null
        }
    },
    "tags" : {},
    "type" : "Microsoft.Compute/virtualMachines",
    "vmId" : "aaaaaaaa-aaaa-aaaa-aaaa-aaaaaaaaaaa",
    "zones" : null,
    "cm" : {
        "kind" : "node",
        "driver" : "azure",
        "cloud" : "az",
        "name" : "testvm1",
        "collection" : "az-node",
        "created" : "2019-04-22 18:16:51.552324",
        "modified" : "2019-04-22 18:16:51.552324"
    }
}
```

## Azure MS Azure Library Provider

The compute provider kind is `MISSING`. The Provider is located at 

* <MISSING>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-cloud/blob/master/cloudmesh/compute/azure/AzProvider.py>


### Flavor

### Image

### VM

## AWS Libcloud Provider

The compute provider kind is `MISSING`. The Provider is located at 

* <MISSING>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-cloud/blob/master/cloudmesh/compute/azure/AzProvider.py>


### Flavor

### Image

### VM

## AWS Boto3 Provider


The compute provider kind is `MISSING`. The Provider is located at 

* <MISSING>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-cloud/blob/master/cloudmesh/compute/azure/AzProvider.py>

### Flavor

### Image

### VM

## Storage


The storage provider kind is `MISSING`. The Provider is located at 

* <MISSING>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-cloud/blob/master/cloudmesh/compute/azure/AzProvider.py>

### Box

The storage provider kind is `box`. The Provider is located at 

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/provider/box/Provider.py>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/Provider.py>


#### Directory

#### File

### Azure Blob


The storage provider kind is `azureblob`. The Provider is located at 

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/provider/azureblob/Provider.py>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/Provider.py>

#### Directory

#### File

### AWSS3 the one from cloudmesh-cloud


The storage provider kind is `awss3`. The Provider is located at 

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/provider/awss3/Provider.py>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/Provider.py>

#### Directory

#### File

### AWSS3 the one from cloudmesh-objstore

It is unclear waht the difference to AWSS3 the one from cloudmesh-cloud is
Please explain. If its the same, let us know and we shoudl merge


The storage provider kind is `objstorage`. The Provider is located at 

* UNCLEAR IF IT DUPLICATES awss3 

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/Provider.py>


#### Directory

#### File


### Google Drive



The storage provider kind is `gdrive`. The Provider is located at 

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/provider/gdrive/Provider.py>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/Provider.py>


#### Directory

#### File

### Local

This has not been tested yet, so be careful as it could remove local dir trees.
we may need ta add an option --force for this provider and always ask if
we wnat to delete the files while shoing them first. This could even be a reason
to introduce it in all providers.



The storage provider kind is `local`. The Provider is located at 

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/provider/local/Provider.py>

This provder should not be used, but you need to use the general provider at

* <https://github.com/cloudmesh/cloudmesh-storage/blob/master/cloudmesh/storage/Provider.py>



#### Directory

#### File



## Workflow

```
/* 2 */
{
    "_id" : ObjectId("5cbc414e20b39a69d014efec"),
    "name" : "b",
    "dependencies" : [
        "c"
    ],
    "workflow" : "workflow",
    "cm" : {
        "kind" : "flow",
        "cloud" : "workflow",
        "name" : "b",
        "collection" : "workflow-flow",
        "created" : "2019-04-21 10:09:18.887115",
        "modified" : "2019-04-21 10:09:18.887115"
    },
    "kind" : "flow",
    "cloud" : "workflow"
}
```

## Emr

## HPC

### Batch

### Queue

### Job

## Keys

```
{
    "_id" : ObjectId("5ca79c92dc64f1905d924234"),
    "name" : "gregor",
    "fingerprint" : "aa:aa:bb:11:22:33:88:98:13:74:8a:3b:6a:5a:b2:5d",
    "public_key" : "ssh-rsa xxxxxxxxx ... gregor@nowhere test",
    "private_key" : null,
    "extra" : {},
    "cm" : {
        "kind" : "key",
        "driver" : "openstack",
        "cloud" : "chameleon",
        "name" : "gregor",
        "collection" : "chameleon-key",
        "created" : "2019-04-05 18:21:06.898856",
        "modified" : "2019-04-06 06:50:30.975625"
    }
}
```