## M-Stack: Free USB Stack for PIC 16F, 18F, 24F, and 32MX Microcontrollers

Forked myself to incorporate a number of forks. 

###Branches

- adilinden, my notes
- master [signal11/m-stack](https://github.com/signal11/m-stack),  
 the original M-Stack from Signal 11.
- pololu [pololu/m-stack](https://github.com/pololu/m-stack),  
 added support for for the PIC18F25K50, PIC18F45K50, and the P-Star 25K50 Micro.
- d235j [d235j/m-stack](https://github.com/d235j/m-stack),  
 added support for the PIC18F87J50.
- hughsie [hughsie/m-stack](https://github.com/hughsie/m-stack),  
 added support for DFU1.1.
- todbot [todbot/m-stack](https://github.com/todbot/m-stack),  
 added support for PIC16F1455.

###Links

- Master page [http://www.signal11.us/oss/m-stack/]
- API Documentation [http://www.signal11.us/oss/m-stack/m-stack/html/group__public__api.html]
- README.txt [https://raw.githubusercontent.com/adilinden/m-stack/master/README.txt]

###Maintain

This is just a note to myself so I don't forget how to do this.

1. Clone the fork
```
git clone git@github.com:adilinden/m-stack.git
cd m-stack
```
2. Create this `README.md` file
```
git checkout -b adilinden 1c51713
```
2. Add all of the other repositories
```
git remote add upstream https://github.com/signal11/m-stack.git
git remote add pololu https://github.com/pololu/m-stack.git
git remote add d235j https://github.com/d235j/m-stack.git
git remote add hughsie https://github.com/hughsie/m-stack.git
git remote add todbot https://github.com/todbot/m-stack.git
```
3. Fetch each and merge into their own branch.
```
git fetch upstream
git checkout master
git merge upstream/master

git fetch pololu
git checkout -b pololu 1c51713
git merge pololu/pull_request_1

git fetch d235j
git checkout -b d235j 1c51713
git merge d235j/pic18f87j50

git fetch hughsie
git checkout -b hughsie 1c51713
git merge hughsie/usb_dfu

git fetch todbot
git checkout -b todbot 1c51713
git merge todbot/master
```
