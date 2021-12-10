
```
# sudo apt update  
# sudo apt install golang
```
```
$ go version 

go version go1.13.8 linux/amd64
```
```
wget https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz
sudo tar -xvf go1.16.4.linux-amd64.tar.gz   
sudo mv go /usr/local 
```

### ~/.profile file.
```
export GOROOT=/usr/local/go
export GOPATH=$HOME/Projects/Proj1
export PATH=$GOPATH/bin:$GOROOT/bin:$PATH
```
