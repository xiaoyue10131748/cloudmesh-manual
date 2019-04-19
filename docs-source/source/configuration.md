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

> STUDENT CONTRIUTE HERE
  
### AWS

> STUDENT CONTRIUTE HERE

### Azure

> STUDENT CONTRIUTE HERE

### Google

> STUDENT CONTRIUTE HERE

### OpenStack

> STUDENT CONTRIUTE HERE

### Virtual Box

> STUDENT CONTRIUTE HERE

### SSH

> STUDENT CONTRIUTE HERE

### Local

> STUDENT CONTRIUTE HERE

### Docker

> STUDENT CONTRIUTE HERE


## Virtual Clusters

> STUDENT CONTRIUTE HERE


## REST

> STUDENT CONTRIUTE HERE

## Log File (proposed)

> THIS FEATURE IS NOT YET SUPPORTED

Log files are stored by default in `~/.cloudmesh/log` The directory can be
specified in the yaml file.

## Encryption 

> STUDENT CONTRIUTE HERE

The yaml file can also be encrypted which is done with the command

```bash
$cms admin encrypt
```

toe edit the file you need to specify a default editor with the shell variable EDITOR.

```bash
export EDITOR=emacs
```

to edit the file you can do it with 

```bash
$ cms admin edit config
```

Once saved you cloudmehs will sheck if your file is encrypted and unencrypt it 
upon start.

It will replace the yaml file with an encryoted version while using your public
private key/ You can keep the file encripted and use the command

```bash
$ ssh-add
```

to access the file without using the password whenefer it is accessed.