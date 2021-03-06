---
title:  What can Azure Backup Server back up | Microsoft Docs
description: This article provides a support matrix listing all workloads, data types, and installations that Azure Backup Server v2 protects.  
services: backup
documentation center: ''
author:  markgalioto
ms.assetid:
ms.service: backup
ms.workload: storage-backup-recovery
keywords:  
ms.date: 05/15/2017
ms.topic:  article
ms.author: markgal,masaran
manager:  carmonm
---

# Azure Backup Server protection matrix

This article lists the various servers and workloads that you can protect with Azure Backup Server. The following matrix lists what can be protected with Azure Backup Server v1 and v2.

## Protection support matrix

|Workload|Version|Azure Backup Server</br> installation|Azure Backup</br> Server v2|Azure Backup</br> Server v1 |Protection and recovery|
|------------|-----------|--------------------|--------------------------------------------|--------------------------------|---------------------------|
|System Center VMM|VMM 2016,<br/>VMM 2012, SP1, R2|Physical server<br /><br />Hyper-V virtual machine|Y|Y|All deployment scenarios: Database|
|Client computers (64-bit and 32-bit)|Windows 10|Physical server<br /><br />Hyper-V virtual machine<br /><br />VMware virtual machine|Y|Y|Files<br /><br />Protected volumes must be NTFS. FAT and FAT32 aren't supported.<br /><br />Volumes must be at least 1 GB. DPM uses Volume Shadow Copy Service (VSS) to take the data snapshot and the snapshot only works if the volume is at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows 8.1|Physical server<br /><br />Hyper-V virtual machine|Y|Y|Files<br /><br />Protected volumes must be NTFS. FAT and FAT32 aren't supported.<br /><br />Volumes must be at least 1 GB. DPM uses Volume Shadow Copy Service (VSS) to take the data snapshot and the snapshot only works if the volume is at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows 8.1|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|Files<br /><br />Protected volumes must be NTFS and at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows 8|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Files<br /><br />Protected volumes must be NTFS and at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows 8|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|Files<br /><br />Protected volumes must be NTFS and at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows 7|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Files<br /><br />Protected volumes must be NTFS and at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows 7|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y |Files<br /><br />Protected volumes must be NTFS and at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows Vista with SP2|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Files<br /><br />Protected volumes must be NTFS and at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows Vista with SP1|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Files<br /><br />Protected volumes must be NTFS and at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows Vista|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Files<br /><br />Protected volumes must be NTFS and at least 1 GB.|
|Client computers (64-bit and 32-bit)|Windows Vista|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Volume, share, folder, file, system state/bare metal), deduped volumes|
|Servers (32-bit and 64-bit)|Windows Server 2016|Azure virtual machine (when workload is running as Azure virtual machine)<br /><br />Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)<br /><br />Physical server<br /><br />On-premises Hyper-V virtual machine|Y<br /><br />Not Nano server|N|Volume, share, folder, file, system state/bare metal), deduped volumes|
|Servers (32-bit and 64-bit)|Windows Server 2012 R2 - Datacenter and Standard|Azure virtual machine (when workload is running as Azure virtual machine)|Y|Y |Volume, share, folder, file<br /><br />DPM must be running on at least Windows Server 2012 R2 to protect Windows Server 2012 deduped volumes.|
|Servers (32-bit and 64-bit)|Windows Server 2012 R2 - Datacenter and Standard|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|Volume, share, folder, file, system state/bare metal)<br /><br />DPM must be running on Windows Server 2012 or 2012 R2 to protect Windows Server 2012 deduped volumes.|
|Servers (32-bit and 64-bit)|Windows Server 2012/2012 with SP1 - Datacenter and Standard|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Volume, share, folder, file, system state/bare metal<br /><br />DPM must be running on at least Windows Server 2012 R2 to protect Windows Server 2012 deduped volumes.|
|Servers (32-bit and 64-bit)|Windows Server 2012/2012 with SP1 - Datacenter and Standard|Azure virtual machine (when workload is running as Azure virtual machine)|Y|Y|Volume, share, folder, file<br /><br />DPM must be running on at least Windows Server 2012 R2 to protect Windows Server 2012 deduped volumes.|
|Servers (32-bit and 64-bit)|Windows Server 2012/2012 with SP1 - Datacenter and Standard|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|Volume, share, folder, file, system state/bare metal<br /><br />DPM must be running on at least Windows Server 2012 R2 to protect Windows Server 2012 deduped volumes.|
|Servers (32-bit and 64-bit)|Windows Server 2008 R2 SP1 - Standard and Enterprise|Physical server<br /><br />On-premises Hyper-V virtual machine|Y<br /><br />You need to be running SP1 and install [Windows Management Frame 4.0](https://www.microsoft.com/en-us/download/details.aspx?id=40855)|Y|Volume, share, folder, file, system state/bare metal|
|Servers (32-bit and 64-bit)|Windows Server 2008 R2 SP1 - Standard and Enterprise|Azure virtual machine (when workload is running as Azure virtual machine)|Y<br /><br />You need to be running SP1 and install [Windows Management Frame 4.0](https://www.microsoft.com/en-us/download/details.aspx?id=40855)|Y |Volume, share, folder, file|
|Servers (32-bit and 64-bit)|Windows Server 2008 R2 SP1 - Standard and Enterprise|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y<br /><br />You need to be running SP1 and install [Windows Management Frame 4.0](https://www.microsoft.com/en-us/download/details.aspx?id=40855)|Y |Volume, share, folder, file, system state/bare metal|
|Servers (32-bit and 64-bit)|Windows Server 2008 R2|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Volume, share, folder, file, system state/bare metal|
|Servers (32-bit and 64-bit)|Windows Server 2008 R2|Azure virtual machine (when workload is running as Azure virtual machine)|N|Y|Volume, share, folder, file|
|Servers (32-bit and 64-bit)|Windows Server 2008 R2|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|N|Y|Volume, share, folder, file, system state/bare metal|
|Servers (32-bit and 64-bit)|Windows Server 2008|Physical server<br /><br />On-premises Hyper-V virtual machine|N|Y|Volume, share, folder, file, system state/bare metal|
|Servers (32-bit and 64-bit)|Windows Server 2008|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y |Volume, share, folder, file, system state/bare metal|
|Servers (32-bit and 64-bit)|Windows Storage Server 2008|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Volume, share, folder, file, system state/bare metal|
|SQL Server|SQL Server 2016|Physical server <br /><br /> On-premises Hyper-V virtual machine <br /> <br /> Azure virtual machine <br /><br /> Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y (UR2 Onwards)|N|All deployment scenarios: database|
|SQL Server|SQL Server 2014|Azure virtual machine (when workload is running as Azure virtual machine)|Y|Y |All deployment scenarios: database|
|SQL Server|SQL Server 2014|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2012 with SP2|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y |All deployment scenarios: database|
|SQL Server|SQL Server 2012 with SP2|Azure virtual machine (when workload is running as Azure virtual machine)|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2012 with SP2|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2012, SQL Server 2012 with SP1|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2012, SQL Server 2012 with SP1|Azure virtual machine (when workload is running as Azure virtual machine)|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2012, SQL Server 2012 with SP1|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2008 R2|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2008 R2|Azure virtual machine (when workload is running as Azure virtual machine)|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2008 R2|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y |All deployment scenarios: database|
|SQL Server|SQL Server 2008|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2008|Azure virtual machine (when workload is running as Azure virtual machine)|Y|Y|All deployment scenarios: database|
|SQL Server|SQL Server 2008|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|All deployment scenarios: database|
|Exchange|Exchange 2016|Physical server<br/><br/> On-premises Hyper-V virtual machine|Y|Y|Protect (all deployment scenarios): Standalone Exchange server, database under a database availability group (DAG)<br /><br />Recover (all deployment scenarios): Mailbox, mailbox databases under a DAG|
|Exchange|Exchange 2016|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|Protect (all deployment scenarios): Standalone Exchange server, database under a database availability group (DAG)<br /><br />Recover (all deployment scenarios): Mailbox, mailbox databases under a DAG|
|Exchange|Exchange 2013|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Protect (all deployment scenarios): Standalone Exchange server, database under a database availability group (DAG)<br /><br />Recover (all deployment scenarios): Mailbox, mailbox databases under a DAG|
|Exchange|Exchange 2013|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y |Protect (all deployment scenarios): Standalone Exchange server, database under a database availability group (DAG)<br /><br />Recover (all deployment scenarios): Mailbox, mailbox databases under a DAG|
|Exchange|Exchange 2010|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Protect (all deployment scenarios): Standalone Exchange server, database under a database availability group (DAG)<br /><br />Recover  (all deployment scenarios):  Mailbox, mailbox databases under a DAG|
|Exchange|Exchange 2010|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y |Protect (all deployment scenarios): Standalone Exchange server, database under a database availability group (DAG)<br /><br />Recover (all deployment scenarios):  Mailbox, mailbox databases under a DAG|
|Exchange|Exchange 2007|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Protect (all deployment scenarios):  Storage group<br /><br />Recover (all deployment scenarios):  Storage group, database, mailbox|
|Exchange|Exchange 2007|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y |Protect (all deployment scenarios):  Storage group<br /><br />Recover (all deployment scenarios):  Storage group, database, mailbox|
|SharePoint|SharePoint 2016|Physical server<br /><br />On-premises Hyper-V virtual machine<br /><br />Azure virtual machine (when workload is running as Azure virtual machine)<br /><br />Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y (UR2 Onwards)|N|Protect (all deployment scenarios):  Farm,  frontend web server content<br /><br />Recover (all deployment scenarios):  Farm, database, web application, file or list item, SharePoint search, frontend web server<br /><br />Note that protecting a SharePoint farm that's using the SQL Server 2012 AlwaysOn feature for the content databases isn't supported.|
|SharePoint|SharePoint 2013|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Protect (all deployment scenarios):  Farm,  frontend web server content<br /><br />Recover (all deployment scenarios):  Farm, database, web application, file or list item, SharePoint search, frontend web server<br /><br />Note that protecting a SharePoint farm that's using the SQL Server 2012 AlwaysOn feature for the content databases isn't supported.|
|SharePoint|SharePoint 2013|Azure virtual machine (when workload is running as Azure virtual machine) - DPM 2012 R2 Update Rollup 3 onwards|Y|Y|Protect (all deployment scenarios):  Farm, SharePoint search, frontend web server content<br /><br />Recover (all deployment scenarios):  Farm, database, web application, file or list item, SharePoint search, frontend web server<br /><br />Note that protecting a SharePoint farm that's using the SQL Server 2012 AlwaysOn feature for the content databases isn't supported.|
|SharePoint|SharePoint 2013|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y |Protect (all deployment scenarios):  Farm, SharePoint search, frontend web server content<br /><br />Recover (all deployment scenarios):  Farm, database, web application, file or list item, SharePoint search, frontend web server<br /><br />Note that protecting a SharePoint farm that's using the SQL Server 2012 AlwaysOn feature for the content databases isn't supported.|
|SharePoint|SharePoint 2010|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Protect (all deployment scenarios): Farm, SharePoint search, frontend web server content<br /><br />Recover (all deployment scenarios): Farm, database, web application, file or list item, SharePoint search, frontend web server|
|SharePoint|SharePoint 2010|Azure virtual machine (when workload is running as Azure virtual machine)|Y|Y |Protect (all deployment scenarios): Farm, SharePoint search, frontend web server content<br /><br />Recover (all deployment scenarios): Farm, database, web application, file or list item, SharePoint search, frontend web server|
|SharePoint|SharePoint 2010|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|Protect (all deployment scenarios): Farm, SharePoint search, frontend web server content<br /><br />Recover (all deployment scenarios): Farm, database, web application, file or list item, SharePoint search, frontend web server|
|SharePoint|SharePoint 2007|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Protect (all deployment scenarios):  Farm, SharePoint search, frontend web server content<br /><br />Recover (all deployment scenarios):  Farm, database, web application, file or list item, SharePoint search, frontend web server|
|SharePoint|SharePoint 2007|Windows virtual machine in VMWare (protects workloads running in Windows virtual machine in VMWare)|Y|Y|Protect (all deployment scenarios):  Farm, SharePoint search, frontend web server content<br /><br />Recover (all deployment scenarios):  Farm, database, web application, file or list item, SharePoint search, frontend web server|
|Hyper-V host - DPM protection agent on Hyper-V host server, cluster, or VM|Windows Server 2016|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|N|Protect: Hyper-V computers, cluster shared volumes (CSVs)<br /><br />Recover: Virtual machine, Item-level recovery of files and folder, volumes, virtual hard drives|
|Hyper-V host - DPM protection agent on Hyper-V host server, cluster, or VM|Windows Server 2012 R2 - Datacenter and Standard|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Protect: Hyper-V computers, cluster shared volumes (CSVs)<br /><br />Recover: Virtual machine, Item-level recovery of files and folder, volumes, virtual hard drives|
|Hyper-V host - DPM protection agent on Hyper-V host server, cluster, or VM|Windows Server 2012 - Datacenter and Standard|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Protect: Hyper-V computers, cluster shared volumes (CSVs)<br /><br />Recover: Virtual machine, Item-level recovery of files and folder, volumes, virtual hard drives|
|Hyper-V host - DPM protection agent on Hyper-V host server, cluster, or VM|Windows Server 2008 R2 SP1 - Enterprise and Standard|Physical server<br /><br />On-premises Hyper-V virtual machine|Y|Y|Protect: Hyper-V computers, cluster shared volumes (CSVs)<br /><br />Recover: Virtual machine, Item-level recovery of files and folder, volumes, virtual hard drives|
|Hyper-V host - DPM protection agent on Hyper-V host server, cluster, or VM|Windows Server 2008|Physical server<br /><br />On-premises Hyper-V virtual machine|N|N|Protect: Hyper-V computers, cluster shared volumes (CSVs)<br /><br />Recover: Virtual machine, Item-level recovery of files and folder, volumes, virtual hard drives|
|Linux|Linux running as Hyper-V guest|On-premises Hyper-V virtual machine|Y|Y|Hyper-V must be running on Windows Server 2012 R2 or Windows Server 2016. Protect: Entire virtual machine<br /><br />Recover: Entire virtual machine|

## Cluster support
Azure Backup Server can protect data in the following clustered applications:

-   File servers

-   SQL Server

-   Hyper-V - If you protect a Hyper-V cluster using scaled-out DPM protection, you can't add secondary protection for the protected Hyper-V workloads.

    If you run Hyper-V on Windows Server 2008 R2, make sure to install the update described in KB [975354](https://support.microsoft.com/en-us/kb/975354).
    If you run Hyper-V on Windows Server 2008 R2 in a cluster configuration, make sure you install SP2 and KB [971394](https://support.microsoft.com/en-us/kb/971394).

-   Exchange Server - Azure Backup Server can protect non-shared disk clusters for supported Exchange Server versions (cluster-continuous replication), and can also protect Exchange Server configured for local continuous replication.

-   SQL Server - Azure Backup Server doesn't support backing up SQL Server databases hosted on cluster-shared volumes (CSVs).

Azure Backup Server can protect cluster workloads that are located in the same domain as the DPM server, and in a child or trusted domain. If you want to protect data sources in untrusted domains or workgroups, use NTLM or certificate authentication for a single server, or certificate authentication only for a cluster.
