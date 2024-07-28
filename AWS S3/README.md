
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

S3 Security

We have different types of protecting the data such as user based policies (IAM) and resource based policies 
encryption - encrypt the objects using encryption keys 

arn:aws:s3:::sg-ssd-spm/*

{
  "Id": "Policy1722141899406",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Stmt1722141897153",
      "Action": [
        "s3:GetObject"
      ],
      "Effect": "Allow",
      "Resource": "arn:aws:s3:::sg-ssd-spm/*",
      "Principal": "*"
    }
  ]
}


S3 Static website hosting :

S3 is also an excellent option for hosting static websites. Static websites do not rely on server-side processing like PHP, JSP, etc.; their pages can contain static content and client-side scripting.

You can use a static website as the entry point into your application, especially if there is a public element to your website that is used to advertise products and services. Because you may not be fully aware of the total traffic likely to hit your website, static websites hosted on Amazon S3 are highly scalable and require minimal management overhead as AWS handles scalability elements in the background.

Once you have enabled static hosting, your S3 bucket will be accessible via a website endpoint URL. This URL can access your website directly, or you can configure a custom domain name using Route53. You will explore Route53 later in this study guide. You can also configure additional options, such as redirects and routing rules, to further customize your website’s behavior.




S3 Bucket versioning :

Amazon S3 versioning allows users to store multiple versions of an object within a single bucket. This feature can be helpful in retrieving previous versions of an object due to unintended changes, user errors, or application errors. When versioning is enabled for a bucket, Amazon S3 keeps multiple copies of the same object, even when numerous write requests are made concurrently.

enabling s3 bucket versioning helps for unintended deletes 
It protects the data from the accidental deletions 
We can also rollback to the any version of data that we needed 

Object Lock:

Another feature of Amazon S3 that helps prevent accidental deletions is Object Lock. This service uses a write-once-read-many (WORM) model to avoid Amazon S3 objects from being deleted or overwritten. Often used in environments where the organization needs to meet regulatory requirements or to add an additional layer of protection. Amazon S3 Object lock is configurable in two ways:

Retention period – where you specify a fixed period during which an object remains locked by either setting retention periods on individual objects or as a default retention period for the whole bucket. You can also configure minimum and maximum allowable retention periods with the s3:object-lock-remaining-retention-days bucket policy conditional statement.
Legal hold – where the object is protected indefinitely with no retention period until you explicitly remove it.
