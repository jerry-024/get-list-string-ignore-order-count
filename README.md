# get-list-string-ignore-order-count
---

1.desc：先对string排序然后在group count
scala 代码事例
```scala
val ls = "abcd" :: "dcab" :: "aadb" :: "daba" :: Nil
ls.map(s => s.sortWith(_ < _)).groupBy(a => a).map(x => (x._1 -> x._2.size))
out: scala.collection.immutable.Map[String,Int] = Map(aabd -> 2, abcd -> 2)
```
2. desc： 将每一个字符映射到一个素数求成绩然后 count

