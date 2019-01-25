Get sourcecode 
```
mkdir -p /usr/local/src/kamailio-5.1
cd /usr/local/src/kamailio-5.1

git clone --depth 1 --no-single-branch https://github.com/altanai/kamailio.git kamailio
 git checkout -b 5.1 origin/5.1
cd kamailio/
```
setup env and dependecies 
```
sudo su
apt update
apt install make gcc build-essential bison flex libmysqlclient-dev 
```
These dependecies are required to build c source code and using header files like mysql.h , pcre.h and libsquirrel

Build 
```
make include_modules="db_mysql dialplan" cfg
make all
```
After succesfull install , all executable will be found  
cd /usr/local/sbin/

