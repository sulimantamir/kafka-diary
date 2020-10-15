# kafka-diary
##First using the confluent platform on RHEL / CENTOS 
##Install the required packages and import the key

sudo yum install curl which
sudo rpm --import https://packages.confluent.io/rpm/6.0/archive.key

##create the confluent.repo file 

[Confluent.dist]
name=Confluent repository (dist)
baseurl=https://packages.confluent.io/rpm/6.0/7
gpgcheck=1
gpgkey=https://packages.confluent.io/rpm/6.0/archive.key
enabled=1

[Confluent]
name=Confluent repository
baseurl=https://packages.confluent.io/rpm/6.0
gpgcheck=1
gpgkey=https://packages.confluent.io/rpm/6.0/archive.key
enabled=1

##Install the community version if you want and that's what i m going to use for my testing

sudo yum clean all &&  sudo yum install confluent-community*
