# astronv
GPU version of astrominer. A Dero GPU miner.

Support channel for this: https://discord.gg/nvgHnwD3rZ

astronv is an optimized GPU miner for DERO (and any forks that use AstroBWTv3)

### Usage ###
To mine on hiveos: COMING SOON


To mine with wss(mining over RPC to your node):
```
eg: ./astronv -w DERO_ADDRESS -r YOUR_NODE:YOUR_PORT -r1 failover_pool_1 -r2 failover_pool_2
```
For further help:

```
./astrominer -h
```

Arguments:
```
	-h	show this message
	-r	pool url (required)
	-r1	failover pool url 1 (optional)
	-r2	failover pool url 2 (optional)
	-w	your wallet (required)
	-p	pool type. stratum or RPC (optional, default: rpc)
	-show-latency	show the latency between miner and pool (doesn't work with Windows Node) 
	-log-interval	time between 2 logging lines in second (default: 5 seconds) 
	-disable-api	Disable miner API on port 60666, this API is required for hiveOS 
	-no-watchdog	Disable astronv watchdog
	-log-to-file	Redirect all astronv log to a file
	-sock-address	Socks5 ip address with port (eg: 127.0.0.1:8192) (default: null)
	-sock-auth	Socks5 username and password (eg: username:password). NOTE: this username and password can't contain space and : symbol (default: null)
	-report-realtime-hashrate	 Enable sending realtime hashrate to hansen33 mod node (default: disable)
	-zero-hr-restart-time	 Time (in second), restart (or exit if the watchdog is disabled) the miner after being zero hashrate for a while (default: 120 seconds, set -1 to disable)
	-b	 Batch number for GPU. Use comma to set different values for multiple gpus (Eg: -b 1000,1100,1200,...)
				 set 0 to disable that GPU, ex: disabling GPU#2 -b 1000,2000,0,3000,4000,...
				 set -1 to auto detect batch size for the GPU, ex: auto detect for GPU#2 -b 1000,2000,-1,3000,4000,... 
				 default: -1 (auto detect for all GPUs)
	-lgc	 Lock gpu graphic clocks, work the same way as nvidia-smi -lgc. Use comma to set different values for multiple gpus (Eg: -lgc 1000,1100,1200,...) [Root permission is required]
	-lmc	 Lock gpu memory clocks, work the same way as nvidia-smi -lmc. Use comma to set different values for multiple gpus (Eg: -lgc 1000,1100,1200,...) [Root permission is required]
	-core-offset	 Set core clocks offset. Use comma to set different values for multiple gpus (Eg: -lgc 100,110,120,...) [Root permission is required]
	-mem-offset	 Set memory clocks offset. Use comma to set different values for multiple gpus (Eg: -lgc 1000,1100,1200,...) [Root permission is required]
```

(bash script files are included with the binary, change your dero address to use it)

### Dev fee ###
dev fee is 4.9%

### Downloads ###
Visit https://github.com/dero-am/astrominer/releases for all available releases.
