# GCP Storage

GCP storage options based on type of data. *Note: Database options are in [Databases](./databases.md)*

## Object Storage

---

## Block Storage

### **Zonal Persistent Disks**

***Data lost during a zone outage***

Offered as:
 - Standard Persistent Disk (HDD)
 - Balanced Persistent Disk *Note: New service - unlikely to be in exam*
 - Performance Persistent Disk (SSD)
 - Extreme Persistent Disk (SSD) *Useful for enterprise databases. e.g Oracle/ SAP HANA*

Important Features:
 - Can be used as boot disk
 - Snapshots for backups
 - Encrypted by Default. Can be encrypted with ***Customer Supplied Keys***
 - Supports ***Dynamic size increase while in use***

### **Regional Persistent Disks**

Regional Persistent Disks provide durable storage and replication of data between ***two zones in the same region.***

Limitations 
 - Not as performant as Zonal Disks
 - Cannot be used as boot disk
 - Minimum Size is 200GB
 - Supported on a limited number of instance types. i.e E2, N1, N2, and N2D machine type VMs.
 - Supports attachment to 10 VMs in ***a read-only mode***


In the unlikely event of a zonal outage, you can usually failover your workload running on regional persistent disks to another zone by using the --force-attach flag. The --force-attach flag lets you attach the regional persistent disk to a standby VM instance even if the disk can't be detached from the original VM due to its unavailability. To learn more, see Regional persistent disk failover. You cannot force attach a zonal persistent disk to an instance.


Important Features
 - Supports incremental snapshots similar to Zonal PD. 
 - ***--force-attach flag*** can be used to attach a regional disk to a standby instance in case of a zonal outage, even if the disk can't be detached from the original VM due to its unavailability



### **Local SSD**

Features
 - Local SSDs are ephemeral in nature. ***Data on local SSD is lost when the instance is stopped or terminated***
 - Offers superior performance, very high IOPS, and very low latency compared to SSD.
 - Each SSD is 375GB, maximum of 24 SSD's can be attached for 9TB per instance
 - Suitable only for temporary storage such as ***caches, processing space/scratch space***