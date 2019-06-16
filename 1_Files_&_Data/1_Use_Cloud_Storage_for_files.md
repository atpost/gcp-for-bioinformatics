# Use Google Cloud File Storage


### Why do this
 - Your workload and data files are too big to run on your laptop
 - You don't want to wait for time on your organization's shared cluster


### What is this
 - Use GCP Cloud Storage buckets to store your files
 - Use GCP Cloud Storage buckets to perform analysis (compute services) on your files


### Key considerations
 - Understanding costs and selecting the best fit type of storage for your data
 - Understanding storage class types (multi-regional, regional, nearline, coldline)
 - Understanding storage location options (shown below)

 [![Cloud Storage regions](/images/regions.png)]()

### How to do this
 - Create a bucket with a unique name
 - Configure the bucket storage class type (see below)
 - Configure the bucket location 
 - Configure the bucket access control, encryption and retention
 - List of key [bucket operations](https://cloud.google.com/storage/docs/how-to)

 [![Cloud Storage types](/images/storage.png)]()

 [![Cloud Storage config](/images/bucket.png)]()


### How to verify you've done it
 - Upload file(s) to the bucket using the web console or the 'gsutil' tool - [link](https://cloud.google.com/storage/docs/gsutil) - example shown below

 [![upload](/images/upload.png)]()


### Other Things to Know
 - Storage can be the most significant GCP service cost for bioinformatics (due to the number and size of files involved in analysis)
 - Select the storage class that fits best for your analysis, i.e. multi-regional, regional....
 - Design file archiving processes, i.e. move to nearline or coldline if not accessing or over time (i.e. monthly...)
 - Delete files generated during processing (often called intermediate files) that are no longer needed when jobs complete

### How to learn more
 - Best practices for Google Cloud Storage - [link](https://cloud.google.com/storage/docs/best-practices)
 - Hosting a static website on Cloud Storage - [link](https://cloud.google.com/storage/docs/hosting-static-website)