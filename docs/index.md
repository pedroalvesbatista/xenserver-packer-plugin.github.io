# Welcome to XenServer/XCP-ng Builder Pacler Plugin


The XenServer Packer builder is able to create XenServer virtual machines and export them either as an XVA or a VDI and create VM templates starting from an ISO image.

The builder builds a virtual machine by creating a new virtual machine from scratch, booting it, installing an OS, provisioning software within the OS, then shutting it down. The result of the XenServer builder is a directory containing all the files necessary to run the virtual machine portably.

