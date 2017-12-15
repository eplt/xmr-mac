# xmr-mac
Binary releases of xmr-stak for macOS.
(Mostly for people who aren't too comfortable with commandline apps.)

# Running **xmr-stak** on macOS

Just been playing around with Monero (XMR) and can't find compiled versions for macOS. So I compiled and shared these binaries for anyone who wants to mine Monero on their computer but don't want to compile their own app. You will still need basic level of understanding of macOS and Terminal app to run these. Credits to the original developers, check out their repo and donate to them accordingly. https://github.com/fireice-uk/xmr-stak 


## Getting started

Start off by installing Brew on your Mac.

Load up Terminal.

Then copy and paste the following command into Terminal and press enter.

```shell
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Download the binaries in this repo to your desktop, or any folder that you know the location of. Change into that directory.

If you know you have NVIDIA GPUs, then copy and paste the following lines to install dependencies you need.

### For NVIDIA GPUs

```shell
brew tap caskroom/drivers
brew cask install nvidia-cuda
brew install hwloc libmicrohttpd openssl
./xmr-stak-nvidia
```

For CPU only mining, then copy and paste the following lines to install dependencies you need.

### For CPU-only mining

```shell
brew install hwloc libmicrohttpd openssl
./xmr-stak
```

### On first start
You will need to get a mining pool address and wallet address ready.
A common pool to use is "pool.minexmr.com:7777". Default password for most miners is "x".
To get your own Monero Wallet, try mymonero.com. [click here](https://cnhv.co/nada). 
:) You are welcome to try it with my wallet too.
```shell
485Y4gAqSbcjAd3Q9cSFzrj6fFFbA2HZ7gmV1vWJAsmpNYfbjJcp9KpFHZJMqLEgjLbfQrD7Xy1nkQYrncNH5KChUWwhKgP
```
Happy mining!

Output from initial start should be something like this:
```shell
./xmr-stak 
Please enter:
- Currency: 'monero' or 'aeon'
monero
- Pool address: e.g. pool.usxmrpool.com:3333
pool.minexmr.com:7777
- Username (wallet address or pool login):
485Y4gAqSbcjAd3Q9cSFzrj6fFFbA2HZ7gmV1vWJAsmpNYfbjJcp9KpFHZJMqLEgjLbfQrD7Xy1nkQYrncNH5KChUWwhKgP
- Password (mostly empty or x):
x
- Does this pool port support TLS/SSL? Use no if unknown. (y/N)
N
- Do you want to use nicehash on this pool? (y/n)
n
- Do you want to use multiple pools? (y/n)
n
Configuration stored in file 'config.txt'
```


