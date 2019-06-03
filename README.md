
# ClassicBets
ClassicBets - P2P Cryptocurrency for classic betting games

Required operating system for ClassicBets wallet and daemon is **Ubuntu 16.04 x64 or higher**

**Cloning the repository and compiling :**
------------------------------------------------------------------------
```
cd
git clone https://github.com/ClassicBets/cbet-coin.git
cd cbet-coin
chmod +x autogen.sh
chmod +x share/genbuild.sh
chmod +x src/leveldb/build_detect_platform
./autogen.sh
./configure
make
make install #optional if you want to install wallet
```
**Installation of dependencies :**
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
**Installing Berkeley DB :**
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
classicbetsd -daemon -listen
```
Stopping the daemon:
-----------
```
classicbets-cli stop
```
Daemon status:
---------------
```
classicbets-cli getinfo
classicbets-cli mnsync status
classicbets-cli masternode status 
```

**All binaries for different operating systems, you can download in the releases repository:**
---------------------------
https://github.com/ClassicBets/cbet-coin/releases

**Connecting ports:**
----------------------------
RPC Port : 7776
P2P Port : 7777

**More informations:**
--------------------
Please , find more informations on our website https://classicbets.net.
Block Explorer : http://explorer.classicbets.net

**CBET Specifications**
---------------------------

<table>
  <tr>
    <td>Coin name :</td>
    <td>ClassicBets</td>
  </tr>
  <tr>
    <td>Abbreviation :</td>
    <td>CBET</td>
  </tr>
  <tr>
    <td>P2P Port :</td>
    <td>7777</td>
  </tr>
  <tr>
    <td>RPC Port :</td>
    <td>7776</td>
  </tr>
  <tr>
    <td>Coin type :</td>
    <td>POS + Masternode</td>
  </tr>
  <tr>
    <td>Algo :</td>
    <td>Quark</td>
  </tr>
  <tr>
    <td>Block time :</td>
    <td>60 Seconds</td>
  </tr>
  <tr>
    <td>Maturity :</td>
    <td>6 Blocks</td>
  </tr>
  <tr>
    <td>MN Confirmations :</td>
    <td>10 Blocks</td>
  </tr>
  <tr>
    <td>Difficulty retargeting :</td>
    <td>10 Blocks</td>
  </tr>
  <tr>
    <td>Masternode collateral :</td>
    <td>3,333 CBET</td>
  </tr>
  <tr>
    <td>Total Coin Supply :</td>
    <td>21,000,000 CBET</td>
  </tr>
  <tr>
    <td>Premine :</td>
    <td>177,777 CBET (0.84%)*</td>
  </tr>
</table>
* Please read informations about premine usage on our website [classicbets.net](https://classicbets.net)
