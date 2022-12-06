# CMPE_283

# Assignment 1

# Discovering VMX Features

## Anupama Ponukumati

1. Created vm using gcp UI with machine configuration as :
Machine type n2-standard-2
CPU platform Intel Cascade Lake Architecture x86/64

2. Executed following commands on console

#gcloud compute instances export instance-5 \
--destination=cmpe283.yaml \
--zone=us-central1-a

3. enabled virtualisation = true in cmpe283.yaml
advancedMachineFeatures: enableNestedVirtualization: true


4. #gcloud compute instances update-from-file instance-5 --source=cmpe283.yaml --most-disruptive-allowed-action=RESTART --zone=us-central1-a


5. Created directory :cmpe283-1

6. Created two files - 
Make file
cmpe283-1.c

for IA32_VMX_PINBASED_CTLS 0x481 IA32_VMX_PROCBASED_CTLS 0x482 IA32_VMX_EXIT_CTLS 0x483 IA32_VMX_ENTRY_CTLS 0x484
IA32_VMX_PROCBASED_CTLS2 0x48B IA32_VMX_PROCBASED_CTLS3 0x492

7. Executed following commands:
#make sudo bash apt install gcc make

    #exit

    #sudo apt install linux-headers-$(uname -r)

    #uname -r

    #make

    #sudo insmod ./cmpe283-1.ko

    #sudo dmesg

## Screenshots of Output

![Screenshot 1](outputImages/img1.png)

![Screenshot 2](outputImages/img2.png)

![Screenshot 3](outputImages/img3.png)




# Assignment 2



# Assignment 3





