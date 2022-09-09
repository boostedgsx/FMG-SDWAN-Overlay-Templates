# FMG-SDWAN-Overlay-Templates
Brief overview of the SDWAN Overlay Templates in FortiManager 7.2

Lab environment consisting of (4) Fortigate VMs running firmware 7.0.6 and (1) FortiManager VM running firmware 7.2.1

All Fortigates are configured with SDWAN and (2) active WAN ports, both behind NAT. Each branch site has (2) active VLANS; VLAN100 and VLAN200.

All IP addresses, hostnames, screenshots, etc are from the lab environment and contain no sensitive environmental information.

<pre>

</pre>

## Configured Metadata variables: 

I've included examples of the metadata variables to give you an idea of how these work as the Fortinet KB doesn't mention much about this, other than the branch_id variable. You can essentially create whatever you want. You're supposed to be able to use these for the interfaces under "Network Advertisements" in the templates, but I wasn't able to get that to work as it was trying to insert the variables into the installation configs which resulted in a failure. So in that case, I just use them for the wan interfaces in production.

### Location of the menu 

![Metadata Variables - Menu Location](https://user-images.githubusercontent.com/72212024/189391791-e867e746-3f17-424b-969e-382a43e99892.png)


### Metadata Variable - wan1

![Metadata Variables - wan1](https://user-images.githubusercontent.com/72212024/189391926-5a251b17-7d02-4a2f-8ed6-a8541ced8aa7.png)


### Metadata Variable - wan2

![Metadata Variables - wan2](https://user-images.githubusercontent.com/72212024/189391949-b4a3e070-319c-4c6a-99d8-b5ac78deb1cd.png)


### Metadata Variable - branch_id

![Metadata Variables - branch_id](https://user-images.githubusercontent.com/72212024/189392008-148b3957-c908-4c6e-8d10-82c0e21dd7f7.png)

<pre>

</pre>

## SD-WAN Overlay Template Configuration Example

This just walks you through the templates to give you an idea of how simple it is to generate and/or modify the current configurations at all of your Hub and Branch sites. Once the template is created, you can modify pretty much all of the settings or update route maps, etc. 

### SDWAN Overlay Template 1 of 5

![SDWAN Overlay Template 1 of 5](https://user-images.githubusercontent.com/72212024/189392389-57ed81ac-accf-436b-b2a1-d23d7b86a829.png)

### SDWAN Overlay Template 2 of 5

![SDWAN Overlay Template 2 of 5](https://user-images.githubusercontent.com/72212024/189392422-36d7ba2c-70f4-43d9-8e4c-75e2d2000610.png)

### SDWAN Overlay Template 3 of 5

![SDWAN Overlay Template 3 of 5](https://user-images.githubusercontent.com/72212024/189392532-97552d43-5e01-4637-8870-e69546193fde.png)

### SDWAN Overlay Template 4 of 5

![SDWAN Overlay Template 4 of 5](https://user-images.githubusercontent.com/72212024/189392613-e6ea73e8-f8c9-49d3-b90b-4225c07ea68a.png)

### SDWAN Overlay Template 5 of 5

![SDWAN Overlay Template 5 of 5](https://user-images.githubusercontent.com/72212024/189392675-2a00e80c-6de5-4fa7-a603-57945bbff350.png)

<pre>


</pre>

## There are (2) example configurations uploaded; "Install ADVPN" and "Install no ADVPN"

I've included screenshots of these two configurations so you can get an idea of what settings I used when generating the templates.


## Install ADVPN

![LAB_SDWAN_OL - Install ADVPN](https://user-images.githubusercontent.com/72212024/189393312-a3b9dd07-2b62-4824-814d-16b81b7d3faa.png)

## Install no ADVPN

![LAB_SDWAN_OL - Install no ADVPN](https://user-images.githubusercontent.com/72212024/189393414-ccc70b70-6207-48d1-a53c-af504d8fa139.png)
