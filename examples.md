# Examples

Examples
In order for new users to get up and running with the packer builder, a few examples of building a machine image with popular distros have been created.

In order to see an exhaustive list of configuration options for the packer builder please see the following documentation. This doc will focus on the details relevant to the particular distro.

Running the examples
In order to run the examples you will need to perform the following steps:

```
Export those vars:
PKR_VAR_remote_host
PKR_VAR_remote_password
PKR_VAR_remote_username
PKR_VAR_sr_name
PKR_VAR_sr_iso_name
PKR_VAR_remote_host must be the resource pool primary, aka the master.
```

Run `packer init path/to/defenition.pkr.hcl` to download the xenserver plugin

Run packer build  path/to/defenition.pkr.hcl

So for example: packer build  examples/centos/centos8-netinstall.pkr.hcl

#### Debian / Ubuntu

The Ubuntu example uses the autoinstall tool to configure the VM template. Please see the autoinstall docs for an exhaustive list of what is supported.

Packer will create a http server to serve the files as specified from the http_directory specified in the builder configuration. This is where the user-data and meta-data for autoinstall must be present.

#### Rocky Linux / CentOS / RHEL

The Rocky Linux / CentOS / RHEL examples use `kickstart` files to configure the VM template. Please see the kickstart documentation for the options that are supported.

Packer will create a http server to serve the files as specified from the http_directory specified in the builder configuration. This is where the kickstart config file must be present.

#### FreeBSD / OpenBSD / NetBSD

* Coming soon !