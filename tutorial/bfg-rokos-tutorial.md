# BFGMiner 550 ROKOS

## Installing Required Libraries

The miner to be installed comes as source files, which means that the program must be compiled into a binary before it can be run. To make a program, in this case BFGMiner, many dependencies are required.

Dependencies are additional software, or libraries the program needs in order to compile properly, as it has been developed using them to make the software more efficient. 

So lets start: In the ROKOS desktop, double click on terminal shortcut and type in the following:

1) sudo apt-get update

2) sudo apt-get install autoconf autogen libtool uthash-dev libjansson-dev libcurl4-openssl-dev libusb-dev libncurses-dev git-core –y

This process will take a few minutes to complete.

## Installing BFGMiner

Once all the dependencies have been installed, now it is time to download and install BFGMiner, so type the following into the Terminal. It’s normal for these to take a few minutes to complete so some patience is needed.

git clone https://github.com/BitcoinFullnode/bfgminer-rokos550

cd bfgminer-rokos550

./autogen.sh

./configure

make

## Start Mining Bitcoin

Now you’re ready to start mining. To do this, providing you're using Slush’s pool, you’ll use the following command:

./bfgminer -o stratum.bitcoin.cz:3333 -O username.worker:password -S all

The username section is composed of two parts, the username that you use to login to the pool, and worker which is the worker name you gave when you registered the worker. Finally, the password that was set when you created the worker.

That’s a lot of numbers, so let's make some of them a bit clearer.

**Current mining speed, typically calculated in megahashes or gigahashes.** 
The number of hashes a second that can be calculated the better. A hash is an algorithm of converting numbers and letters into an undecryptable set of characters. So a miner is used to process millions of numbers in an effort to match the hash to guess the original number. The more hashes that can be processed the faster it is able to solve the problem.

**Number of accepted shares.** 
A share on a pool is to show the miner has successfully worked out a given problem, so the more shares you can process the better your reward from the pool.

**Detailed information on accepted shares and pool updates.** 
This is a running log of what is currently happening with the miners and basic pool information, such as messages of updates and when new blocks are found.


## Conclusion

Following these steps will leave you with a very energy efficient bitcoin miner, as a Raspberry Pi only uses four watts of power, and a miner is typically 2.5W. Mining used to be done with computers consuming over 700W for the same process so to make a jump in savings helps repay the cost of the hardware we are using.

All there is to do now is to sit back and watch the Bitcoin slowly build up. Though it is important that you understand that Bitcoin value fluctuates wildly, it is extremely volatile, so invest at your own risk. 
