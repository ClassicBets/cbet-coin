
# ClassicBets
CHVCash - ChainVertizer Exchange Network Crypto Currency

Required operating system : **Ubuntu 16.04 & 18.04 x64**

**Important note:**
---------------
Before you receive your first CHVCash coins in your wallet , **disable** Zerocoin protocol 
(zCHVCash autominting) in your wallet.
How to :
1. In QT Wallet :
- Wallet menu -> Settings -> Options
- Uncheck "Enable zCHVC automint"
2. In command line wallet/daemon , VPS :
- stop wallet (daemon)
- open and edit chvcash.conf file in CHVCash main directory
- insert "enablezeromint=0" to configuration file
- save configuration file
- restart your wallet (daemon)

**Cloning the repository and compiling (use any user with the sudo group):**
------------------------------------------------------------------------
```
cd
git clone https://github.com/ChainVertizer/CHVCash.git
cd CHVCash
chmod +x autogen.sh
chmod +x share/genbuild.sh
chmod +x src/leveldb/build_detect_platform
./autogen.sh
./configure
make
make install #optional
```
**Installation of libraries (using root user):**
---------------------------
```
sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3 libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev libboost-all-dev libboost-program-options-dev
sudo apt-get install libminiupnpc-dev libzmq3-dev libprotobuf-dev protobuf-compiler unzip software-properties-common
sudo apt-get install build-essential libtool autotools-dev autoconf pkg-config libssl-dev libevent-dev
sudo apt-get install libboost-all-dev
sudo apt-get install libdb4.8-dev libdb4.8++-dev
sudo apt-get install libminiupnpc-dev
sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler
sudo apt-get install libqrencode-dev
```
**Installing Berkeley DB (using root user):**
---------------------------
```
wget https://download.oracle.com/berkeley-db/db-4.8.30.zip
unzip db-4.8.30.zip
cd db-4.8.30
cd build_unix/
../dist/configure --prefix=/usr/local --enable-cxx
make
sudo make install
```
Running the daemon:
-------------------
```
chvcashd -daemon
```
Stopping the daemon:
-----------
```
chvcash-cli stop
```
Daemon status:
---------------
```
chvcash-cli getinfo
chvcash-cli mnsync status
chnvash-cli masternode status
```

**All binaries for different operating systems, you can download in the releases repository:**
---------------------------
https://github.com/ChainVertizer/CHVCash/releases

**Connecting ports:**
----------------------------
RPC Port : 8183
P2P Port : 8184

**More informations:**
--------------------
Please , find more informations on our website https://chvcash.com or on CHVCash & ChainVertizer support Discord server https://discord.gg/75CRAFC . 
Chain monitor is located here : https://chvcashexplorer.com

