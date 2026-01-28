# Unit 7.1 - UFM as a Docker Installation Prerequisites

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



```
cat /etc/*rel* ## 1. Ensure both linux are running same linux distro

## 2. Install docker (if not installed)
sudo apt install docker.io
service docker status

docker pull hello-world ## test

## 3.
apt-get install pacemaker pcs drbd-utils
apt list --installed | grep pacemaker
apt list --installed | grep pcs
apt list --installed | grep drbd-utils

## 4. check space available (10-20 GB)
lsblk

## 5. 
ping <server>

## 6.
hostname -i
cat /etc/hosts

ifconfig ib0

## 7.
mkdir /opt/ufm_files/
mkdir /tmp/ufm_lic/

## 8.
cp /auto/UFM/UFM_SW/lic/volt-ufm.... /tmp/ufm_lic

## 9. Verify which ethernet interface for ufm HA
route | grep -ml default | awk '{print $NF}' (output could be ensl60)
```



