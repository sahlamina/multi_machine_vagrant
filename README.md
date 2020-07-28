# Multi Machine Exercise
---
## Objectives of this exercise
### Creating a second virtual machine named "db" and running it simultaneously
### Configuring the db machine with a different IP address from the app  
### Provision the db machine with a mongoDB database

---
### Creating a second Virtual Machine (VM) called "db"
* The first step was downloading the multi-machine-start-code zip file and unzipping it
* Next I researched how to enable my Vagrantfile capable of running two files at once
* I did this by defining the config.vm line as 'db' and making sure the following lines of code were consistent with the db. prefix
* I also amended the IP address in this step by simply changing the last three numbers of the IP address string
* I ran the ```vagrant up``` command and saw two VMs were created which meant that my exercise was working as exected
---
### Provisioning the db machine with a mongoDB database
* I researched the syntax an method for installing mongoDB and after trial and error with a few sources, I found a good source and pasted it into my provision.sh file
* The provision.sh file can be located in the environment directory -> app -> provision.sh
* I then ran ```vagrant destroy``` followed by ```vagrant up``` to see if my code had been affected and if my two VMs were unaffected by my changes
---
### Testing the database is functional
* Next, I tested  that all my installed packages were working correctly
* To do this, I navigated to the tests directory and ran the ```rake spec``` command
* The test resulted in 9 examples and 0 failures for my app and 4 examples with 0 failures for my db

