# wasmminer

## build wsproxy and run

```
sudo apt install golang
export GOPATH=~/go
go get github.com/gorilla/websocket
cd wsproxy
go build
./wsproxy
```

## run HTTP server

```
sudo apt install apache2
```
 and add these line to /etc/apache2/apache2.conf
```
<Directory /Path/to/wasmminer>
   Options Indexes FollowSymLinks
   AllowOverride ALL
   Require all granted
</Directory>
```
 and edit /etc/apache2/sites-available/000-default.conf line 12 like this
```
   DocumentRoot /Path/to/wasmminer
```



## build cpuminer/wasm and install

* see https://github.com/ohac/cpuminer
* copy `wasmminer.wasm`, `wasmminer.js`, `em.js` and `worker.js` to js directory
