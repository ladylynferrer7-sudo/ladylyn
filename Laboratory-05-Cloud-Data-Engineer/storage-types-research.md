# Research: Types of Cloud Storage

## Cloud Storage Comparison

| **Storage Type** | **Description (How it stores data)** | **Primary Use Case** | **Cloud Provider Example** |
|---|---|---|---|
| **Block Storage** | Splits data into fixed-size blocks with unique identifiers. Acts like raw, unformatted hard drives attached to a server. | High-performance databases, virtual machine boot volumes, and operating systems. | AWS EBS (Elastic Block Store) |
| **File Storage** | Organizes data hierarchically in a shared folder structure using file paths and directories, similar to a traditional shared drive. | Centralized file sharing, content management systems, and legacy application storage. | AWS EFS (Elastic File System) |
| **Object Storage** | Stores data as discrete objects containing raw payload data, customizable metadata, and a unique identifier within a flat namespace. | Unstructured media files such as images and videos, backups, logs, and big data storage. | AWS S3 / MinIO |

---

## Client Recommendation

**Object Storage** is the ideal choice for storing millions of user-uploaded images because it uses a flat and highly scalable namespace rather than a restrictive file-system hierarchy.

Unlike block storage, which typically requires managing allocated volumes and capacity, object storage is designed to scale to very large amounts of unstructured data without complex drive partitioning or storage management.

Additionally, object storage allows custom metadata to be attached to each photo. This can help applications organize, index, retrieve, and serve images efficiently through web application APIs.

### Why Object Storage?

- **Highly scalable** – Designed to handle large amounts of unstructured data.
- **Easy to manage** – Does not require traditional file-system hierarchies.
- **Metadata support** – Allows additional information to be associated with stored objects.
- **Suitable for media** – Well-suited for images, videos, documents, backups, and logs.
- **Web-friendly** – Can be integrated with applications through APIs.

