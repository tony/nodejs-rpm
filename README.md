# NodeJS v0.9.0

Built for CentOS v5.5.

* node.js rpm spec: https://github.com/tony/nodejs-rpm
* node.js source: http://nodejs.org/dist/

Source tgz file from: http://nodejs.org/dist/

# compile `sed` locally

```bash
cd /usr/local/bin
wget ftp://ftp.gnu.org/gnu/sed/sed-4.2.1.tar.gz
cd sed-4.2.1
./configure
make
make install
```

# node-js

```bash
curl -sR -o /usr/src/redhat/SOURCES/node-v0.9.0.tar.gz http://nodejs.org/dist/v0.9.0/node-v0.9.0.tar.gz
curl -sR -o /usr/src/redhat/SPECS/nodejs.spec https://raw.github.com/tony/nodejs-rpm/master/nodejs.spec
rpmbuild -ba /usr/src/redhat/SPECS/nodejs.spec
yum localinstall --nogpgcheck /usr/src/redhat/RPMS/`arch`/nodejs-v0.9.rpm
```

# todo

* update spec support later distributions of CentOS, Fedora that support `sed -E`