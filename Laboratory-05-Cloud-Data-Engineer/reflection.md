# Mission 5 Reflection: The Cloud Data Engineer

### 1. Why is object storage better suited for storing millions of photos compared to a traditional block storage hard drive?

Object Storage is better suited for storing millions of photos because it is designed to handle large amounts of unstructured data. Unlike Block Storage, which works more like a virtual hard drive with allocated storage volumes, Object Storage stores each photo as an individual object with its own identifier and metadata. It is also highly scalable, making it more practical for applications that continuously receive many user-uploaded images.

### 2. How did using Docker make it easier to deploy the MinIO storage server?

Using Docker made deploying MinIO much easier because I did not have to manually install all the required dependencies and configure the server step by step. I only needed to use the `docker run` command with the required ports and environment variables. It made the deployment faster and helped me understand how containers can make software easier to set up and run.

### 3. What is a "bucket" in the context of cloud storage?

A bucket is a logical container used to store and organize objects in Object Storage. In this activity, I created a bucket named `client-photos` and uploaded a sample file into it. I learned that buckets help organize stored data and can also be used with access and security settings.

### 4. How do you think large enterprise companies ensure their object storage data is not lost if the physical server crashes?

Large enterprise companies can protect their data by keeping multiple copies and using technologies such as replication and erasure coding. These methods allow data to remain available or be recovered even when some physical drives or servers fail. Data can also be stored across different locations so that one hardware failure will not cause all the stored data to be lost.

### 5. How is your confidence in navigating the Linux command line growing?

My confidence in using the Linux command line is growing because this activity allowed me to use actual Docker and Linux commands instead of only learning about them theoretically. At first, commands such as `docker run`, `-p`, `-e`, and `docker ps` were confusing to me. After using them and seeing the MinIO server successfully running, I became more comfortable understanding what each command and option does. This laboratory made me realize that practice is important, and it gave me more confidence in working with Linux, Docker, and cloud infrastructure.
