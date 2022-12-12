# binance-prepump-monitor

A very simple C++ program I used to catch pre-pumps back in 2021 when there were several large groups of pump&dump conspirators active. 

Run a couple minutes before the actual "pump", specify the volatility on which it should act (0.5%,1%,2% etc), the buy amount denoted in BTC, and the sell premium.

Once it detects a (pre-)pump it will immediately buy and and relist the "asset" for the specified premium. 
Usually your buy order will be the first one filled after the insider pre-pump, however if the pump is too weak or has no pre-pump you will sometimes still be left holding the bag.

Ideally you want to run this on an EC2 instance in JPY (Or wherever your crypto exchange is hosted, in my case binance) as latency was key to beating other people doing the same thing.

I don't remember the exact api commands, but you should be able to graph your entry quite easily for statistical purposes.

![mega2102](https://user-images.githubusercontent.com/120112097/207094289-552a1848-e2b3-4c2b-be47-023cd2c3f1b4.png)
I don't recall what discord this was from (21/02 February 2021, Blue is entry/exit) Every black dot represents a trade.

Note that I only ever used this as a proof of concept. 
