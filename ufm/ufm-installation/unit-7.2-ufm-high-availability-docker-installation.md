# Unit 7.2 - UFM High-Availability Docker Installation

docker run -it --rm --name=ufm installer -v /var/run/docker.sock: /var/run/docker.sock -v /opt/ufm files/:/ins tallation/ufm files/ -v /tmp/ufm lic/:/installation/ufm licenses/ m ellanox/ufm-enterprise-installer:latest - -install -m SA - -auto-star t no -e mellanox/ufm-enterprise: latest - -mgmt-interfac ens160



above flags correspond to the dir and folders obtained from previous stage



2. Download HA package and extract
3. run install shell script
4. Start standby server & use standby configuration script
