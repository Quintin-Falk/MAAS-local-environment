# MAAS-local-environment
<h2>The creation of a MAAS environment</h2>

**Creating the local environment:** 
The first part of this project was creating a local environment to test creating the "Rocky Linux" image within MAAS. This was done through an ubuntu desktop and used an lxd host to creat VMs within MAAS. VMs were then composed, deployed, and tested. 

<h3>Installed ubuntu onto a desktop following the directions from the ubuntu website</h3>
	
 	https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview

<h3>Installed multipass on ubuntu desktop</h3>
	
 	sudo snap install multipass 

<h3>Created a MAAS instance with the yaml file given at https://raw.githubusercontent.com/canonical/maas-multipass/main/maas.yml</h3>	
 	
	wget -qO- https://raw.githubusercontent.com/canonical/maas-multipass/main/maas.yml \
 	| multipass launch --name maas -c4 -m8GB -d32GB --cloud-init -

<h4>-Signed into MAAS UI with ip from the instance</h4>

<h4>-Login with user "admin" and password "admin"</h4>

<h4>-Wait for the stock image to finish downloading onto maas</h4>

<h4>-Compose a VM with the LXD host</h4>

<h4>-Deploy that VM with ubuntu image to make sure that VM's are running correctly</h4>

**<h2>Testing:</h2>**
<h4>-Pinging and ssh into the ip of the newly created VM</h4>
