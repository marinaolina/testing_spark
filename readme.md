# testing_spark
Few examples of spark code that gives different results in local and cluster mode with multiple executors

## basics about cluster and client mode
https://medium.com/@sephinreji98/understanding-spark-cluster-modes-client-vs-cluster-vs-local-d3c41ea96073

## example from documentation
https://spark.apache.org/docs/3.4.1/rdd-programming-guide.html#understanding-closures-

Key Takeaways
 - In local mode, the execution is sequential, leading to consistent, predictable updates to the accumulator.
 - In cluster mode, due to parallel execution, task retries, and optimizations, updates to the accumulator may be inconsistent.
Accumulators should preferably be used in actions rather than transformations to ensure consistency.