
# ClassicBets
ClassicBets - P2P Cryptocurrency for classic betting games

Required operating system for ClassicBets wallet and daemon is **Ubuntu 16.04 x64 or higher**

**Cloning the repository and compiling**
------------------------------------------------------------------------
```
cd
git clone https://github.com/ClassicBets/cbet-coin.git
cd cbet-coin
chmod +x autogen.sh configure share/genbuild.sh src/leveldb/build_detect_platform
./autogen.sh
./configure
make
make install #optional if you want to install wallet
```
**Installation of dependencies**
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
**Installing Berkeley DB**
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
Running the daemon
-------------------
```
classicbetsd -daemon -listen
```
Stopping the daemon
-----------
```
classicbets-cli stop
```
Daemon status
---------------
```
classicbets-cli getinfo
classicbets-cli mnsync status
classicbets-cli masternode status 
```

**All binaries for different operating systems, you can download in the releases repository**
---------------------------
https://github.com/ClassicBets/cbet-coin/releases

**Connecting ports**
----------------------------
RPC Port : 7776
P2P Port : 7777

**More informations**
--------------------
Please , find more informations on our website https://classicbets.net.
Block Explorer : http://explorer.classicbets.net

**CBET Specifications**
---------------------------

<table>
  <tr>
    <td>Coin name</td>
    <td>ClassicBets</td>
  </tr>
  <tr>
    <td>Abbreviation</td>
    <td>CBET</td>
  </tr>
  <tr>
    <td>P2P Port</td>
    <td>7777</td>
  </tr>
  <tr>
    <td>RPC Port</td>
    <td>7776</td>
  </tr>
  <tr>
    <td>Coin type</td>
    <td>POS + Masternode</td>
  </tr>
  <tr>
    <td>Algo</td>
    <td>Quark</td>
  </tr>
  <tr>
    <td>Block time</td>
    <td>60 Seconds</td>
  </tr>
  <tr>
    <td>Maturity</td>
    <td>6 Blocks</td>
  </tr>
  <tr>
    <td>MN Confirmations</td>
    <td>10 Blocks</td>
  </tr>
  <tr>
    <td>Difficulty retargeting</td>
    <td>10 Blocks</td>
  </tr>
  <tr>
    <td>Masternode collateral</td>
    <td>3,333 CBET</td>
  </tr>
  <tr>
    <td>Total Coin Supply</td>
    <td>21,000,000 CBET</td>
  </tr>
  <tr>
    <td>Premine</td>
    <td>177,777 CBET (0.84%)*</td>
  </tr>
  <tr>
    <td>POS Reward</td>
    <td>25 %</td>
  </tr>
<tr>
    <td>MN Reward</td>
    <td>75 %</td>
  </tr>
<tr>
    <td>Zero Protocol</td>
    <td>Disabled for 2Y</td>
  </tr>
</table>
* Please read informations about premine usage on our website https://classicbets.net


**Reward Distribution**
----------------------------

<table>
<thead>
  <tr>
    <th scope="col">Block No</th>
    <th scope="col">Reward / Block</th>
    <th scope="col">POS Reward</th>
    <th scope="col">MN Reward</th>
  </tr>
<thead>
<tbody>
<tr>
  <th scope="row">1-720</th>
  <th scope="row">1 CBET</th>
  <td>--PREMINE--</td>
  <td>--PREMINE--</td>
  </tr>
<tr>
  <th scope="row">720-12,160</th>
  <th scope="row">0.10 CBET</th>
  <td>0.025 CBET</td>
  <td>0.075 CBET</td>
  </tr>
<tr>
  <th scope="row">12,161-22,160</th>
  <th scope="row">01.00 CBET</th>
  <td>0.250 CBET</td>
  <td>0.750 CBET</td>
  </tr>
  <tr>
  <th scope="row">22,161-32,240</th>
  <th scope="row">1.50 CBET</th>
  <td>0.375 CBET</td>
  <td>1.125 CBET</td>
  </tr>
  <tr>
  <th scope="row">32,241-42,320</th>
  <th scope="row">1.75 CBET</th>
  <td>0.437 CBET</td>
  <td>1.312 CBET</td>
  </tr>
  <tr>
  <th scope="row">42,321-52,400</th>
  <th scope="row">2.00 CBET</th>
  <td>0.500 CBET</td>
  <td>1.500 CBET</td>
  </tr>
  <tr>
  <th scope="row">52,401-62,480</th>
  <th scope="row">2.25 CBET</th>
  <td>0.562 CBET</td>
  <td>1.687 CBET</td>
  </tr>
  <tr>
  <th scope="row">62,481-72,560</th>
  <th scope="row">2.50 CBET</th>
  <td>0.625 CBET</td>
  <td>1.875 CBET</td>
  </tr>
  <tr>
  <th scope="row">72,561-82,640</th>
  <th scope="row">2.75 CBET</th>
  <td>0.687 CBET</td>
  <td>2.063 CBET</td>
  </tr>
  <tr>
  <th scope="row">82,641-92,720</th>
  <th scope="row">3.00 CBET</th>
  <td>0.750 CBET</td>
  <td>2.250 CBET</td>
  </tr>
  <tr>
  <th scope="row">92,721-102,800</th>
  <th scope="row">3.25 CBET</th>
  <td>0.812 CBET</td>
  <td>2.438 CBET</td>
  </tr>
  <tr>
  <th scope="row">102,801-112,880</th>
  <th scope="row">3.50 CBET</th>
  <td>0.875 CBET</td>
  <td>2.625 CBET</td>
  </tr>
    <tr>
  <th scope="row">112,881-122,960</th>
  <th scope="row">3.75 CBET</th>
  <td>0.937 CBET</td>
  <td>2.813 CBET</td>
  </tr>
    <tr>
  <th scope="row">122,961-143,120</th>
  <th scope="row">4.00 CBET</th>
  <td>1.000 CBET</td>
  <td>3.000 CBET</td>
  </tr>
    <tr>
  <th scope="row">143,121-163,280</th>
  <th scope="row">4.50 CBET</th>
  <td>1.125 CBET</td>
  <td>3.375 CBET</td>
  </tr>
    <tr>
  <th scope="row">163,281-183,440</th>
  <th scope="row">5.00 CBET</th>
  <td>1.250 CBET</td>
  <td>3.750 CBET</td>
  </tr>
    <tr>
  <th scope="row">183,441-203,600</th>
  <th scope="row">6.00 CBET</th>
  <td>1.500 CBET</td>
  <td>4.500 CBET</td>
  </tr>
     <tr>
  <th scope="row">203,601-213,680</th>
  <th scope="row">5.75 CBET</th>
  <td>1.437 CBET</td>
  <td>4.312 CBET</td>
  </tr>
      <tr>
  <th scope="row">213,681-223,760</th>
  <th scope="row">5.50 CBET</th>
  <td>1.375 CBET</td>
  <td>4.125 CBET</td>
  </tr>
      <tr>
  <th scope="row">223,761-233,840</th>
  <th scope="row">5.25 CBET</th>
  <td>1.312 CBET</td>
  <td>3.937 CBET</td>
  </tr>
      <tr>
  <th scope="row">233,841-243,920</th>
  <th scope="row">5.00 CBET</th>
  <td>1.250 CBET</td>
  <td>3.750 CBET</td>
  </tr>
      <tr>
  <th scope="row">243,921-254,000</th>
  <th scope="row">4.75 CBET</th>
  <td>1.187 CBET</td>
  <td>3.562 CBET</td>
  </tr>
      <tr>
  <th scope="row">254,001-264,080</th>
  <th scope="row">4.50 CBET</th>
  <td>1.125 CBET</td>
  <td>3.375 CBET</td>
  </tr>
        <tr>
  <th scope="row">264,081-274,160</th>
  <th scope="row">4.25 CBET</th>
  <td>1.062 CBET</td>
  <td>3.187 CBET</td>
  </tr>
        <tr>
  <th scope="row">274,161-284,240</th>
  <th scope="row">4.00 CBET</th>
  <td>1.000 CBET</td>
  <td>3.000 CBET</td>
  </tr>
        <tr>
  <th scope="row">284,241-294,320</th>
  <th scope="row">3.75 CBET</th>
  <td>0.937 CBET</td>
  <td>2.812 CBET</td>
  </tr>
        <tr>
  <th scope="row">294,321-304,400</th>
  <th scope="row">3.50 CBET</th>
  <td>0.875 CBET</td>
  <td>2.625 CBET</td>
  </tr>
        <tr>
  <th scope="row">304,401-314,480</th>
  <th scope="row">3.25 CBET</th>
  <td>0.812 CBET</td>
  <td>2.437 CBET</td>
  </tr>
        <tr>
  <th scope="row">314,481-324,560</th>
  <th scope="row">3.00 CBET</th>
  <td>0.750 CBET</td>
  <td>2.250 CBET</td>
  </tr>
        <tr>
  <th scope="row">324,561-334,640</th>
  <th scope="row">2.75 CBET</th>
  <td>0.687 CBET</td>
  <td>2.062 CBET</td>
  </tr>
        <tr>
  <th scope="row">334,641-344,720</th>
  <th scope="row">2.50 CBET</th>
  <td>0.625 CBET</td>
  <td>1.875 CBET</td>
  </tr>
        <tr>
  <th scope="row">344,721-354,800</th>
  <th scope="row">2.25 CBET</th>
  <td>0.562 CBET</td>
  <td>1.687 CBET</td>
  </tr>
        <tr>
  <th scope="row">354,801-364,880</th>
  <th scope="row">2.00 CBET</th>
  <td>0.500 CBET</td>
  <td>1.500 CBET</td>
  </tr>
        <tr>
  <th scope="row">364,881-374,960</th>
  <th scope="row">1.75 CBET</th>
  <td>0.437 CBET</td>
  <td>1.312 CBET</td>
  </tr>
        <tr>
  <th scope="row">374,961-1,051,200</th>
  <th scope="row">1.50 CBET</th>
  <td>0.375 CBET</td>
  <td>1.125 CBET</td>
  </tr>
  <tr>
    <th scope="row" colspan=4>Then reward is halving every two years</th>
  <tr>
</tbody>
</table>


**Super Blocks**
-----------------

<table>
<thead>
  <tr>
    <th scope="col">Block No</th>
    <th scope="col">Reward / Block</th>
    <th scope="col">POS Reward</th>
    <th scope="col">MN Reward</th>
  </tr>
<thead>
<tbody>
  <tr>
    <td>
27000,37000,47000,57000<br/>
67000,77000,87000,97000<br/>
107000,117000,127000,137000<br/>
147000,157000,167000,177000<br/>
187000,197000,207000,217000<br/>
227000,237000,247000,257000<br/>
267000,277000,287000,297000<br/>
307000,317000,327000,337000<br/>
347000,357000,367000,377000      
    </td>
    <td>77.00 CBET</td>
    <td>19.25 CBET</td>
    <td>57.75 CBET</td>
  </tr>
</tbody>
</table>


**Ultra Blocks**
-----------------

<table>
<thead>
  <tr>
    <th scope="col">Block No</th>
    <th scope="col">Reward / Block</th>
    <th scope="col">POS Reward</th>
    <th scope="col">MN Reward</th>
  </tr>
<thead>
<tbody>
  <tr>
    <td>
25,000      
    </td>
    <td>177.00 CBET</td>
    <td>44.25 CBET</td>
    <td>132.75 CBET</td>
  </tr>
  <tr>
    <td>
50,000      
    </td>
    <td>277.00 CBET</td>
    <td>69.25 CBET</td>
    <td>207.75 CBET</td>
  </tr>
  <tr>
    <td>
75,000      
    </td>
    <td>377.00 CBET</td>
    <td>94.25 CBET</td>
    <td>282.75 CBET</td>
  </tr>
  <tr>
    <td>
100,000      
    </td>
    <td>477.00 CBET</td>
    <td>119.25 CBET</td>
    <td>357.75 CBET</td>
  </tr>
  <tr>
    <td>
125,000      
    </td>
    <td>577.00 CBET</td>
    <td>144.25 CBET</td>
    <td>432.75 CBET</td>
  </tr>
  <tr>
    <td>
150,000      
    </td>
    <td>677.00 CBET</td>
    <td>169.25 CBET</td>
    <td>507.75 CBET</td>
  </tr>
  <tr>
    <td>
175000,200000,225000<br/>
250000,275000,300000<br/>
325000,350000,375000<br/>
400000,425000,450000<br/>
475000,500000,525000<br/>
550000,575000,600000<br/>
    </td>
    <td>777.00 CBET</td>
    <td>194.25 CBET</td>
    <td>582.75 CBET</td>
  </tr>
</tbody>
</table>


