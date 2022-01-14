* **Spark**: open-source cluster computing framework with
**in-memory data processing engine** used to do ETL, Machine Learning and Analytics Jobs on large volumes of data at rest (Batch processing) or in motion (Streaming).

* **What's the difference with Hadoop**: in contrast to Hadoop’s two-stage disk-based MapReduce computation engine, Spark's multi-stage (mostly) in-memory computing engine allows for running most computations in memory, and hence most of the time provides better performance for certain applications.

* Spark provides an efficient abstraction for in-memory cluster computing called **Resilient Distributed Dataset**.

* Apache Spark uses a scheduler, **DAGScheduler**: It postpones any processing until really required for actions. Spark's lazy evaluation gives plenty of opportunities to induce low-level optimizations.

* **Supported Data Processing**: Spark offers three kinds of data processing using batch, interactive, and stream processing with the unified API and data structures.

* **Spark has better I/O perfomance than Hadoop**: In the no-so-long-ago times, when the most prevalent distributed computing framework was MapReduce, you could reuse a data between computation (even partial ones!) only after you've written it to an external storage like Hadoop Distributed Filesystem (HDFS)]. It can cost you a lot of time to compute even very basic multi-stage computations. It simply suffers from I/O (and perhaps network) overhead. 

    * Spark cuts it out in a way to keep as much data as possible in memory and keep it there until a job is finished. It doesn't matter how many stages belong to a job. What does matter is the available memory and how effective you are in using Spark API (so no shuffle occur).