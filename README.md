## Deploying Standalone VM-Series in vSphere##
Skillet to configure Panorama NSX-T plugin.
The skillet will configure both service definition and service manager sections. 

## prerequisites ##

To run this skillet you will need
1. A template stack to which the VM-Series firewalls will be assigned.
2. A device group or device group hierarchy to which these VM-Series firewalls will be assigned.

## Usage ##

1- Import this repo into your panhandler.

2- Run the skillet and fill the following fields and click submit (Make sure to add quotes if the value will contain space):
  - name: template_stack
    description: Select the template stack to which the VM-Series firewalls will be assigned.
  - name: device_group
    description: Select the device group or device group hierarchy to which these VM-Series firewalls will be assigned
  - name: ovf_url
    description: Enter the URL (IP address or host name and path) where the NSX Manager can access the OVF file to provision new VM-Series firewalls.
  - name: svc_definition
    description: Enter the name for the service you want to display on the NSX Manager.
  - name: svc_manager
    description: Enter a name to identify the VM-Series firewall as a service. This name displays on the NSX Manager and is used to deploy the VM-Series firewall on-demand.
  - name: svc_manager_url
    description: Specify the URL that Panorama will use to establish a connection with the NSX Manager.
  - name: svc_manager_user
    description: Enter the authentication username configured on the NSX Manager.
  - name: svc_manager_pass
    description: Enter the authentication password configured on the NSX Manager.

3- Fill in Panorama IP, Username and Password on the PAN-OS utils section and then click Submit.

4- Validate the changes in Panorama.

## Support Policy

The code and templates in the repo are released under an as-is, best effort,
support policy. These scripts should be seen as community supported and
Palo Alto Networks will contribute our expertise as and when possible.
We do not provide technical support or help in using or troubleshooting the
components of the project through our normal support options such as
Palo Alto Networks support teams, or ASC (Authorized Support Centers)
partners and backline support options. The underlying product used
(the VM-Series firewall) by the scripts or templates are still supported,
but the support is only for the product functionality and not for help in
deploying or using the template or script itself. Unless explicitly tagged,
all projects or work posted in our GitHub repository
(at https://github.com/PaloAltoNetworks) or sites other than our official
Downloads page on https://support.paloaltonetworks.com are provided under