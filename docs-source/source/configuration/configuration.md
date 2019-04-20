# Configuration

The Configuration of cloudmesh is controled with a yaml file that is placed in
`~/.clloudmesh/cloudmesh4.yaml`. It is created automatically from the templace
located at

* <https://github.com/cloudmesh/cloudmesh-cloud/blob/master/cloudmesh/etc/cloudmesh4.yaml>

You can customize the file in your local directory.

## MongoDB

The cache of cloudmesh is managed in a mongo db database with various
collections. However the user does not have to manage thes collections as this
is done for the user through cloudmesh. Before you can use it it mongo does need to be installed.

If you have not installed mongo, you may try 

```bash
$ cms admin mongo install
```

Next you create the database template with authentication with 

```bash
$ cms admin mongo create
```

Now you are ready to use it in cloudmesh.
The mongo db can be started and stoped
with the command

```bash
$cms admin mongo start
$cms admin mongo stop
```

The configuration detals are included in the yaml file.


## Compute Cloud Providers

The default yaml file includes templates to configure various clouds. YOu can
change these defaults and provide access to your cloud credentials to make the
management of cloud virtual machines easier. Templates for AWS, Azure, Google,
OpenStack are provided. Specific templates for Jetstream and Chameleopn cloud
are included

>  STUDENT CONTRIBUTE HERE
  
### AWS

It is beyond the scope of this manual to discuss how to get an account on Aws.
However we do provide a convenient documentation at <STUDENT CONTRUBTE LINK>

>  STUDENT CONTRIBUTE HERE

see Openstack example


### Azure

It is beyond the scope of this manual to discuss how to get an account on Azure.
However we do provide a convenient documentation at <STUDENT CONTRUBTE LINK>

>  STUDENT CONTRIBUTE HERE

see Openstack example

### Google

It is beyond the scope of this manual to discuss how to get an account on Google.
However we do provide a convenient documentation at <STUDENT CONTRUBTE LINK>

>  STUDENT CONTRIBUTE HERE

see Openstack example

### OpenStack

We provide an example on how to use an OpenStack based cloud in cloudmesh.
Please ass the following to your `cloudmesh4.yaml` file and replace the values
for `TBD`. Our example uses [Chameleon Cloud](https://www.chameleoncloud.org/).
This is a cloud for academic research. Certainly you can configure other clouds
based on this template. We have successfully used also clouds in Canada
(Cybera), Germany (KIT), Indiana University (jetstream). TO get started you can
even install your local cloud with devstack and make adjustements. Please
remember you can have multiple clouds in the `cloudmesh4.yaml` file so you could
if you have access to them integrate all of them.

Example for chameleon cloud:

* You will need access to a project and add your project nump=ber to the
  credentials.

```
cloudmesh:
  ...
  cloud:
    ...
    chameleon:
      cm:
        active: True    
        heading: Chameleon
        host: chameleoncloud.org
        label: chameleon
        kind: openstack
        version: liberty
      credentials:
        OS_AUTH_URL: https://openstack.tacc.chameleoncloud.org:5000/v2.0/tokens
        OS_USERNAME: TBD
        OS_PASSWORD: TBD
        OS_TENANT_NAME: CH-819337
        OS_TENANT_ID: CH-819337
        OS_PROJECT_NAME: CH-819337
        OS_PROJECT_DOMAIN_ID: default
        OS_USER_DOMAIN_ID: default
        OS_VERSION: liberty
        OS_REGION_NAME: RegionOne
        OS_KEY_PATH: ~/.ssh/id_rsa.pub
      default:
        flavor: m1.small
        image: CC-Ubuntu16.04
        username: cc        
```

### Virtual Box

>  STUDENT CONTRIBUTE HERE

### SSH

>  STUDENT CONTRIBUTE HERE

### Local

>  STUDENT CONTRIBUTE HERE

### Docker

>  STUDENT CONTRIBUTE HERE







### Storage Providers

General description for all storage providers, comment on the `default:` and
what that does


### AWS S3

>  STUDENT CONTRIBUTE HERE


It is beyond the scope of this manual to discuss how to get an account on Google.
However we do provide a convenient documentation at <STUDENT CONTRUBTE LINK>


In the `cloudmesh4.yaml` file, the 'aws' section under 'storage' describes an
example configuration or a AWS S3 storage provider. In the credentials section
under aws, specify the access key id and secret access key which will be
available in the AWS console under AWS IAM `service` -> `Users` -> `Security
Credentials`. Container is the default Bucket which will be used to store the
files in AWS S3. Region is the geographic area like `us-east-1` which contains
the bucket. Region is required to get a connection handle on the S3 Client or
resource for that geographic area. Here is a sample.

TODO: Make credentials more uniform between compute and data

```bash
storage:
    aws:
      cm:
        heading: aws
        host: amazon.aws.com
        label: aws
        kind: awsS3
        version: TBD
      default:
        directory: /
      credentials:
        access_key_id: *********
        secret_access_key: *******
        container: name of bucket that you want user to be contained in.
        region: Specfiy the default region eg us-east-1
```


### Azure

>  STUDENT CONTRIBUTE HERE

It is beyond the scope of this manual to discuss how to get an account on Google.
However we do provide a convenient documentation at <STUDENT CONTRUBTE LINK>

The `cloudmesh4.yaml` file needs to be set up as follows for the 'azure-blob'
section under 'storage'.

```bash
cloudmesh:
  .........
  storage:
    box:
      cm:
        heading: Box
        host: box.com
        label: Box
        kind: box
        version: TBD
      default:
        directory: TBD
      credentials:
        name: TBD
    azure:
      cm:
        heading: Azure
        host: azure.com
        label: Azure
        kind: azureblob
        version: TBD
      default:
        directory: /
      credentials:
        account_name: '*****************'
        account_key: '********************************************************************'
        container: 'azuretest'
```

Configuration settings for credentials in the yaml file can be obtained from Azure portal.

TODO: MOre information via a pointer to a documentation you create needs to be added here

In the yaml file the following values have to be changed

* `account_name` - This is the name of the Azure blob storage account.
* `account_key` - This can be found under 'Access Keys' after navigating to the storage account on the Azure portal.
* `container` - This can be set to a default container created under the Azure blob storage account.


### Google (BUG)

>  STUDENT CONTRIBUTE HERE


## Google drive

Due to bugs in the requirements of the google driver code, 
we have not yet included it in the Provider code. This needs to be fixed 
before we can do this.

The `cloudmesh4.yaml` file needs to be set up as follows for the 'gdrive'
section under 'storage'.

```bash
storge:
    gdrive: 
      cm: 
        heading: GDrive
        host: gdrive.google.com
        kind: gdrive
        label: GDrive
        version: TBD
      credentials: 
        auth_host_name: localhost
        auth_host_port: 
          - ****
          - ****
        auth_provider_x509_cert_url: "https://www.googleapis.com/oauth2/v1/certs"
        auth_uri: "https://accounts.google.com/o/oauth2/auth"
        client_id: *******************
        client_secret: ************
        project_id: ************
        redirect_uris: 
          - "urn:ietf:wg:oauth:2.0:oob"
          - "http://localhost"
        token_uri: "https://oauth2.googleapis.com/token"
      default: 
        directory: TBD
```


### Box

>  STUDENT CONTRIBUTE HERE

It is beyond the scope of this manual to discuss how to get an account on Google.
However we do provide a convenient documentation at <STUDENT CONTRUBTE LINK>


In the `cloudmesh4.yaml` file, find the 'box' section under 'storage'. Under
credentials, set `config_path` to the path of the configuration file you created
as described in the Box chapter:

```bash
   box:
      cm:
        heading: Box
        host: box.com
        label: Box
        kind: box
        version: TBD
      default:
        directory: /
      credentials:
        config_path: ******************************
```



ADD OTHERS IF MISSING

## Object Store

>  STUDENT CONTRIBUTE HERE


## Virtual Clusters

>  STUDENT CONTRIBUTE HERE



## REST

>  STUDENT CONTRIBUTE HERE

## Log File (proposed)

> THIS FEATURE IS NOT YET SUPPORTED

Log files are stored by default in `~/.cloudmesh/log` The directory can be
specified in the yaml file.

