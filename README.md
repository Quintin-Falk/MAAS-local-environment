# MAAS-local-environment
<h2>The creation of a MAAS environment</h2>

**Creating the local environment:** 
creating a local environment to test new images. This was done through an ubuntu desktop and used an lxd host to creat VMs within MAAS. This was done on a ubuntu desktop with virtualization enabled.

<h3>Installed multipass on ubuntu desktop</h3>
	
 	sudo snap install multipass 

<h3>Created a MAAS instance with the yaml file given at https://raw.githubusercontent.com/canonical/maas-multipass/main/maas.yml</h3>	
 	
	wget -qO- https://raw.githubusercontent.com/canonical/maas-multipass/main/maas.yml \
 	| multipass launch --name maas -c4 -m8GB -d32GB --cloud-init -

Sign into MAAS UI with ip from the instance

Login with user "admin" and password "admin"

Wait for the stock image to finish downloading onto maas

Compose a VM with the LXD host

Deploy that VM with ubuntu image to make sure that VM's are running correctly

**<h2>Testing:</h2>**
<h4>-Pinging and ssh into the ip of the newly created VM</h4>
