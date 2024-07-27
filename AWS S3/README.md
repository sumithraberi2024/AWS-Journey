
What is Amazon S3?

Amazon S3 is a widely used object storage solution with high levels of security, scalability, and durability, making it a preferred choice for businesses of all sizes and industries. With Amazon S3, you can secure your data both in-transit and at rest thanks to the tight integration with Amazon Key Managed Service (Amazon KMS) which offers encryption services. In addition, your objects are replicated and stored across multiple devices, across multple availability zones within a given region, offering the higher levels of durability. Organizations use it for various purposes, such as data lakes, disaster recovery, log archiving, mobile applications, and big data analytics. Amazon S3 also offers tools for optimizing, organizing, and customizing data access based on commercial, organizational, and regulatory requirements


Amazon S3 comprises of four primary concepts:

Buckets - act as the primary container for objects.

Objects - contain the actual data and metadata.

Keys - unique identifiers for each object within a bucket

Region - denotes the geographic location where the bucket is stored.


Amazon S3 Use cases :

1. It is widely used for backup and storage
2. Disaster recovery  - For example, you will move your data to another region.In case a region goes down,then your data is backed up somewhere else.
3. Archieve - You can archieve files in amazon s3 and retrieve it later for much much cheaper
4. Hybrid cloud storage - In case you have storage in on premices and you wont expand it into the cloud then you can use amazon S3.
5. Application and media hosting - To host the applications or to host the media files etc
6. Date lake - To store lot of data and to perform big analytics to deliver a softwares
7. Hosting static websites so on .

S3 Buckets: 

1.S3 allows people to store objects (files) in the buckets (directories)
2.S3 bucket names must be unique globally 
3.Buckets are defined at the region level 
4.S3 looks like a global service but buckets are created at the regional level 
5.S3 buckets naming conventions should not contain uppercase and underscore, should not start with prefix xn-- and must not end with the suffix s3alias
EX : sumithra-tst--database-backups

S3 Objects:

1.Objects(files) have a key 
2. max object size is 5TB (5000GB)
3.If uploading more than 5GB then must use multi part upload
4.Objects has metadata and tags (tags are useful for security and lifecyle)
5.It has version id if versioning is enabled


