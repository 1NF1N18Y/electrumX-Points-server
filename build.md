
echo 'requires Python3.9'
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libsqlite3-dev libreadline-dev libffi-dev curl libbz2-dev -y
  wget https://www.python.org/ftp/python/3.9.1/Python-3.9.1.tgz
  tar -xvf Python-3.9.1.tgz 
  cd Python-3.9.1/
  ./configure --enable-optimizations
  make -j4
  make install

mkdir /var/electrumx-db

echo '
edit electrumx.source to your rpc user and rpcpassword for 9332
 nano electrumx.source 
'
  cp -rf banner.txt /etc/
  apt install python3-pip python3-leveldb libleveldb-dev
   python3.9 -m pip install .
  

  
  
 
  source electrumx.source 
 
  echo 'dont forget to run this
  echo "ulimit -n 10000" >> ~/.bash_profile
  source ~/.bash_profile
'
  echo 'run compact server
    ./electrumx_compact_history
'
    ./electrumx_compact_history



    openssl genrsa -out server.key 2048 && openssl req -new -key server.key -out server.csr && openssl x509 -req -days 1825 -in server.csr -signkey server.key -out server.crt
    cp -rf server.csr /etc/
    cp -rf server.crt /etc/
  
    echo '
    run the server with 
    ./electrumx_server 
