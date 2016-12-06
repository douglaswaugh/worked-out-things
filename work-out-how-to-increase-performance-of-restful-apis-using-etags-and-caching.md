Work out how to increase performance of RESTful APIs using ETags and caching
===

Info Q have an interesting [article][1] on the matter, which confirmed what I was thinking.  There are two ways to improve performance on the server using ETags.

1. Improve bandwidth
2. Improve CPU cycles

Improve bandwidth
---

This can be done by hashing the entire response.

### Pros

Easy to implement
Saves bandwidth

### Cons

Have to get the whole response each time to work out if it's changed

Improve CPU cycles
---

This can be done by keeping track of the version of a resource, and using this in the ETag hashing algorithm. 

### Pros

Saves bandwidth
Saves CPU cycles

### Cons

Could be complicated to implement, depending on why your resource might change

[1]: https://www.infoq.com/articles/etags "Using ETags to Reduce Bandwith & Workload with Spring & Hibernate"