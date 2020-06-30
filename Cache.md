### Cache
#### Having one node and database
You can place the cache in memory or on the local disk of the node. It will be faster than going to the 
network storage
and retrieving the value.
#### Having more nodes and database
When placing the cache on the nodes itself, and the load balancer will randomly distribute to other nodes, 
you will have lots of cache misses.
#### Solutions: global cache and distributed cache
#### Cache Invalidations: keep the cache in-sync with the main storage
##### Write-through cache
Update both database and cache before responding. Has a negative effect on the writing operation.
##### Write-around cache
Update database only. The risk is that the data in the cache is outdated.
##### Write-back cache
Update cache only. The risk is that data can be lost as it only exists in the cache for a while.
#### Cache eviction policies
- First In First Out (FIFO): The cache evicts the first block accessed first without 
any regard to how often or how many times it was accessed before.
- Last In First Out (LIFO): The cache evicts the block accessed most recently first without 
any regard to how often or how many times it was accessed before.
- Least Recently Used (LRU): Discards the least recently used items first.
- Most Recently Used (MRU): Discards, in contrast to LRU, the most recently used items first.
- Least Frequently Used (LFU): Counts how often an item is needed. 
Those that are used least often are discarded first.
- Random Replacement (RR): Randomly selects a candidate item and discards it to make space when necessary.