cotdsa.github.com
=================

To use the repo:

echo "deb http://cotdsa.github.com/debian squeeze main" > /etc/apt/sources.list.d/cotdsa.list
wget -O - http://cotdsa.github.com/cotdsa.gpg | apt-key add -
apt-get update

To add a new package:

dpkg-sig --sign builder /tmp/mypackage_0.1.2_amd64.deb
cd ubuntu && reprepro --ask-passphrase -Vb . includedeb precise /tmp/mypackage_0.1.2_amd64.deb

#Superceded keys:
apt-key del 6AA5E619
