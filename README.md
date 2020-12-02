# docker-compose-confluent

- Step 1 -> export HOST_NAME_1=XX, export HOST_NAME_2=yy, export HOST_NAME_3=zz, export HOST_NAME_4=aa and export LOCAL_CERTS_LOCATION=/location
- Step 2 -> In order to generate certs you will need to run the certs-ca.sh to generate a Root CA certificate and then run "certs-create-per-host.sh HOST_NAME" script for each host you want to generate a certificate for.
- Step 3 -> Copy the generated certs to the each of the VM's
- Step 4 -> run docker-compose-up -d in the zookeeper-vm1 folder, then the broker-vm1 folder, then the control-center-vm1 folder on the first VM
- Step 5 -> run docker-compose-up -d in the zookeeper-vm2 folder, then the broker-vm2 folder on the second vm
- Step 6 -> run docker-compose-up -d in the zookeeper-vm3 folder, then the broker-vm3 folder on the third vm
- Step 7 -> run docker-compose-up -d in the broker-vm4 folder on the fourth vm (edited) 
