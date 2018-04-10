## M-Stack: Free USB Stack for PIC 16F, 18F, 24F, and 32MX Microcontrollers

Forked to incorporate a number of 3rd party forks. 

### Branches

- [adilinden](https://github.com/adilinden/m-stack/tree/adilinden), my notes
- [master](https://github.com/adilinden/m-stack/tree/master) - source is [signal11/m-stack](https://github.com/signal11/m-stack),  
 the original M-Stack from Signal 11.
- [pololu](https://github.com/adilinden/m-stack/tree/pololu) - source is [pololu/m-stack](https://github.com/pololu/m-stack),  
 added support for for the PIC18F25K50, PIC18F45K50, and the P-Star 25K50 Micro.
- [d235j](https://github.com/adilinden/m-stack/tree/d235j) - source is [d235j/m-stack](https://github.com/d235j/m-stack),  
 added support for the PIC18F87J50.
- [hughsie](https://github.com/adilinden/m-stack/tree/hughsie) - source is [hughsie/m-stack](https://github.com/hughsie/m-stack),  
 added support for DFU1.1.
- [todbot](https://github.com/adilinden/m-stack/tree/todbot) - source is [todbot/m-stack](https://github.com/todbot/m-stack),  
 added support for PIC16F1455.

### Links

- Master Page [http://www.signal11.us/oss/m-stack/]
- API Documentation [http://www.signal11.us/oss/m-stack/m-stack/html/group__public__api.html]
- README.txt [https://raw.githubusercontent.com/adilinden/m-stack/master/README.txt]
- Polulo Instructions [https://www.pololu.com/docs/0J62/8]

### Maintain

This is just a note to myself so I don't forget how to do this.

1. Clone the fork

        git clone -o github git@github.com:adilinden/m-stack.git
        cd m-stack

2. Create this `README.md` file

        git checkout -b adilinden 1c51713

2. Add all of the other repositories

        git remote add upstream https://github.com/signal11/m-stack.git
        git remote add pololu https://github.com/pololu/m-stack.git
        git remote add d235j https://github.com/d235j/m-stack.git
        git remote add hughsie https://github.com/hughsie/m-stack.git
        git remote add todbot https://github.com/todbot/m-stack.git

3. Fetch each and merge into their own branch.

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

4. All of the remotes.

        adi@Nebulous: git remote -v
        d235j   https://github.com/d235j/m-stack.git (fetch)
        d235j   https://github.com/d235j/m-stack.git (push)
        github  git@github.com:adilinden/m-stack.git (fetch)
        github  git@github.com:adilinden/m-stack.git (push)
        hughsie https://github.com/hughsie/m-stack.git (fetch)
        hughsie https://github.com/hughsie/m-stack.git (push)
        origin  ssh://git@home/git/forked-github/m-stack.git (fetch)
        origin  ssh://git@home/git/forked-github/m-stack.git (push)
        pololu  https://github.com/pololu/m-stack.git (fetch)
        pololu  https://github.com/pololu/m-stack.git (push)
        todbot  https://github.com/todbot/m-stack.git (fetch)
        todbot  https://github.com/todbot/m-stack.git (push)
        upstream    https://github.com/signal11/m-stack.git (fetch)
        upstream    https://github.com/signal11/m-stack.git (push)
