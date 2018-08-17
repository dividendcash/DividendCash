Dividendcash Core (fork PIVX) integration/staging repository
======================================
***

Quick installation of the Dividendcash daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    sudo add-apt-repository ppa:bitcoin/bitcoin -y
    sudo apt-get update
    export LC_ALL=C
    sudo apt-get install -y zip unzip build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev libdb4.8-dev libdb4.8++-dev


Cloning the repository and compiling (use any user with the sudo group):

    cd /home/
    git clone https://github.com/dividendcash/dividendcash.git
    cd dividendcash
    ./autogen.sh
    ./configure
    sudo make install
    cd /usr/local/bin/
    sudo strip dividendcash*
    cd ..

Running the daemon:

    dividendcashd

Stopping the daemon:

    dividendcash-cli stop

Demon status:

    dividendcash-cli getinfo
    dividendcash-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/dividendcash/dividendcash/releases

P2P port: 19997, RPC port: 19998

### Coin Specs
<table>
<tr><td>Algo</td><td>Quark</td></tr>
<tr><td>Block Time</td><td>60 Seconds</td></tr>
<tr><td>Difficulty Retargeting</td><td>Every Block</td></tr>
<tr><td>Max Coin Supply (PoW Phase)</td><td>165.501 DVD</td></tr>
<tr><td>Max Coin Supply (PoS Phase)</td><td>21.210.101 DVD</td></tr>
<tr><td>Premine</td><td>165.301 DVD</td></tr>
</table>

### Reward Distribution
<table>
<tr><td><b>◆BLOCK HEIGHT</b></td><td><b>◆POW(%)</b></td><td><b>◆MN(%)</b></td><td><b>◆BLOCK REWARD</b></td><td><b>◆POW REWARD</b></td><td><b>◆MN REWARD</b></td></tr>
<tr><td>◆1</td><td>100</td><td>0</td><td>165.301</td><td>165.301</td><td>0</td></tr>
<tr><td>◆2-200</td><td>10</td><td>90</td><td>1</td><td>0.1</td><td>0.9</td></tr>
</table>

<table>
<tr><td><b>◆BLOCK HEIGHT</b></td><td><b>◆POS(%)</b></td><td><b>◆MN(%)</b></td><td><b>◆BLOCK REWARD</b></td><td><b>◆POS REWARD</b></td><td><b>◆MN REWARD</b></td></tr>
<tr><td>◆201-10000</td><td>10</td><td>90</td><td>1</td><td>0.1</td><td>0.9</td></tr>
<tr><td>◆10001-30000</td><td>10</td><td>90</td><td>25</td><td>2.5</td><td>22.5</td></tr>
<tr><td>◆30001-85001</td><td>10</td><td>90</td><td>12</td><td>1.2</td><td>10.8</td></tr>
<tr><td>◆85002-610601</td><td>20</td><td>80</td><td>7</td><td>1.4</td><td>5.6</td></tr>
<tr><td>◆610602-1136201</td><td>20</td><td>80</td><td>6</td><td>1.2</td><td>4.8</td></tr>
<tr><td>◆1136202-1661801</td><td>20</td><td>80</td><td>5</td><td>1</td><td>4</td></tr>
<tr><td>◆1661802-2713001</td><td>20</td><td>80</td><td>4</td><td>0.8</td><td>3.2</td></tr>
<tr><td>◆2713002-3764201</td><td>20</td><td>80</td><td>3</td><td>0.6</td><td>2.4</td></tr>
<tr><td>◆3764202-5341001</td><td>20</td><td>80</td><td>2</td><td>0.4</td><td>1.6</td></tr>
</table>
