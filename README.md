# get-list-string-ignore-order-count
---

1.desc：先对string排序然后在group count

scala 代码事例
```scala
val ls = "abcd" :: "dcab" :: "aadb" :: "daba" :: Nil
ls.map(s => s.sortWith(_ < _)).groupBy(a => a).map(x => (x._1 -> x._2.size))
out: scala.collection.immutable.Map[String,Int] = Map(aabd -> 2, abcd -> 2)
```
2. desc： 将每一个字符映射到一个ASCII码求成绩然后 count
```scala
val ls = "abcd" :: "dcab" :: "aadb" :: "daba" :: Nil
ls.map(s => s.map(_.toInt).reduce(_ * _) -> s).groupBy(a => a._1)map(a => a._2.head._2 -> a._2.size)
res15: scala.collection.immutable.Map[String,Int] = Map(aadb -> 2, abcd -> 2)
```

