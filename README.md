# get-list-string-ignore-order-count
---
```scala
val ls = "abcd" :: "dcab" :: "aadb" :: "daba" :: Nil
ls.map(s => s.sortWith(_ < _)).groupBy(a => a).map(x => (x._1 -> x._2.size))
out: scala.collection.immutable.Map[String,Int] = Map(aabd -> 2, abcd -> 2)
```
get string count in list ignore string order
