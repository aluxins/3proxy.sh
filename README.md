# 3proxy.sh - bash script to install and setup 3proxy

## Supported OS
* Centos 7

## Functional
* Install 3proxy.
* Remove 3proxy
* Add the specified number of users
* Delete one or all users
* Re-issue all users

## How to install

```
curl -O https://raw.githubusercontent.com/aluxins/3proxy.sh/master/3proxy.sh
chmod +x 3proxy.sh
```
Run 3proxy.sh
## PS
* Register the correct name servers by looking at them on your server in /etc/resolv.conf and replace the values of "nserver" in 3proxy.sh

```
nano /etc/resolv.conf
 _____________________
|  nserver 8.8.8.8    |
|  nserver 77.88.8.8  |
 ‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾
```
* To enable logging, replace log /dev/null with:

```
log /var/log/3proxy/3proxy.log D
logformat "- +_L%t.%. %N.%p %E %U %C:%c %R:%r %O %I %h %T"
```

* The configuration file is located here /etc/3proxy.cfg
