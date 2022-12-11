# postgrsql-14_ubuntu_22-04
sudo apt update && sudo apt -y full-upgrade
[ -f /var/run/reboot-required ] && sudo reboot -f

sudo apt install vim curl wget gpg gnupg2 software-properties-common apt-transport-https lsb-release ca-certificates
$ apt policy postgresql
curl -fsSL https://www.postgresql.org/media/keys/ACCC4CF8.asc|sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/postgresql.gpg
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
sudo apt update
Hit:1 http://apt.postgresql.org/pub/repos/apt jammy-pgdg InRelease
sudo apt install postgresql-14
systemctl status postgresql@14-main.service
sudo -u postgres psql -c "SELECT version();"
========================================
https://computingforgeeks.com/install-postgresql-14-on-ubuntu-jammy-jellyfish/
=====================
remove 
https://askubuntu.com/questions/32730/how-to-remove-postgres-from-my-installation
=========================
Ubuntu 20_04
https://techviewleo.com/how-to-install-postgresql-database-on-ubuntu/
