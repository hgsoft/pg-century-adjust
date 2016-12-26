pg-century-adjust
===================
Adjust of default century conversion 2 digits to 4

#Steps to Compile on CentOS 7.2:

```
- Install packages needs to compile:
yum install wget make gcc tar gzip bzip2 readline readline-devel zlib perl perl-libs perl-devel perl-ExtUtils-Embed python python-devel gettext gettext-common-devel gettext-devel gettext-libs openssl openssl-libs openssl-devel openldap openldap-devel pam pam-devel krb5-libs krb5-devel flex flex-devel bison bison-devel tcl tcl-devel libxml2 libxml2-devel libxslt libxslt-devel

- Download the Postres 9.5.5 version:
wget -c https://ftp.postgresql.org/pub/source/v9.5.5/postgresql-9.5.5.tar.bz2

- Untar Postgres:
tar -jxvf postgresql-9.5.5.tar.bz2

- Copy files from this project on the Postgres Source directory:
cp pg-century-adjust/* postgresql-9.5.5/* -R

- Prepare your installation:
./configure --prefix=/usr/pgsql-9.5.5-hg --enable-nls --with-perl --with-python --with-openssl --with-pam --with-ldap --with-readline --with-libxml --with-libxslt

- Run make world:
make world

- Run make check:
make check

- Run make install-world:
make install-world
```
