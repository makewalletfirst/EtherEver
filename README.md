#install dependencies <br>
wget https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz 
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.21.0.linux-amd64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
source ~/.bashrc
go version
<br>

#build <br>
make geth
<br>



#execute <br>
./build/bin/geth console
<br>

#default directory <br>
/root/.ethereum
<br>

#command <br>
admin.nodeInfo.enode
net.peerCount
admin.peers
<br>

