Setup local development environment.  Installs Apache, PHP, Postgres, Symfony.  See ncctest.yml for more details.

*HOST(mac)

- download virtualbox
- download vagrant
- vagrant box add {{ centos7 box }}
- mkdir centos7 && cd centos7
- vagrant init
- vim Vagrantfile
- vagrant up

*GUEST(centos7.0)

- sudo yum install -y git
- git clone https://github.com/masuko-servithink/centos7-symfony.git

- cd centos7-symfony
- ./run.sh
- exec $SHELL -l
- download {{ project file }}

*TROUBLE-SHOOTING

- vagrant plugin install vagrant-vbguest
- vagrant vbguest
- vagrant reload
- vagrant ssh
- sudo yum install -y ftp://ftp.icm.edu.pl/vol/rzm5/linux-slc/centos/7.1.1503/os/x86_64/Packages/kernel-devel-3.10.0-229.el7.x86_64.rpm
