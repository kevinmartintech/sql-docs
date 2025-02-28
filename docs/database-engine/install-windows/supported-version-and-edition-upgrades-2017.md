---
title: "Supported version and edition upgrades (SQL Server 2017)"
description: The supported version and edition upgrades for SQL Server 2017. 
ms.custom: "seo-lt-2019"
ms.date: "12/13/2019"
ms.prod: sql
ms.reviewer: ""
ms.technology: install
ms.topic: conceptual
helpviewer_keywords: 
  - "components [SQL Server], adding to existing installations"
  - "versions [SQL Server], upgrading"
  - "upgrading SQL Server, upgrades supported"
  - "cross-language support"
ms.assetid: 702359c4-6ca9-42a8-860c-a95a802898a1
author: MikeRayMSFT
ms.author: mikeray
monikerRange: ">=sql-server-2016"
---
# Supported version & edition upgrades (SQL Server 2017)

[!INCLUDE [SQL Server -Windows Only](../../includes/applies-to-version/sql-windows-only.md)]
  
  You can upgrade from [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)], [!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)], [!INCLUDE[ssSQL11](../../includes/sssql11-md.md)], [!INCLUDE[ssSQL14](../../includes/sssql14-md.md)], and [!INCLUDE[sssql15-md](../../includes/sssql16-md.md)]. This article lists the supported upgrade paths from these [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] versions, and the supported edition upgrades for [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)].  
  
## Pre upgrade Checklist  
  
-   Before upgrading from one edition of [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] to another, verify that the functionality you are currently using is supported in the edition to which you are moving.  
  
-   Before upgrading [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], enable Windows Authentication for [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Agent and verify the default configuration: that the [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Agent service account is a member of the [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] sysadmin group.  
  
-   To upgrade to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)], you must be running a supported operating system. For more information, see [Hardware and Software Requirements for Installing SQL Server](../../sql-server/install/hardware-and-software-requirements-for-installing-sql-server.md).  
  
-   Upgrade will be blocked if there is a pending restart.  
  
-   Upgrade will be blocked if the Windows Installer service is not running.  
  
## Unsupported Scenarios  
  
-   Cross-version instances of [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] are not supported. Version numbers of the [!INCLUDE[ssDE](../../includes/ssde-md.md)] components must be the same in an instance of [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)].  
  
-   [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] is only available for 64-bit platforms. Cross-platform upgrade is not supported. You cannot upgrade a 32-bit instance of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] to native 64-bit using [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Setup. However, you can back up or detach databases from a 32-bit instance of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], and then restore or attach them to a new instance of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] (64-bit) if the databases are not published in replication. You must re-create any logins and other user objects in master, msdb, and model system databases.  
  
-   You cannot add new features during the upgrade of your existing instance of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. After you upgrade an instance of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)], you can add features by using the [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Setup. For more information, see [Add Features to an Instance of SQL Server &#40;Setup&#41;](./add-features-to-an-instance-of-sql-server-setup.md).  
 
-   Failover Clusters are not supported in WOW mode.  
    
## Upgrades from Earlier Versions to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)]  
 
[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] supports upgrade from the following versions of SQL Server:
 
- SQL Server 2008 SP4 or later
- SQL Server 2008 R2 SP3 or later
- SQL Server 2012 SP2 or later
- SQL Server 2014 or later 
- SQL Server 2016 or later
 

  
> [!NOTE]  
>  To upgrade databases on [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] see [Support for 2005](#SupportFor2005).  
  
 The table below lists the supported upgrade scenarios from earlier versions of [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)].  
  
|Upgrade from|Supported upgrade path|  
|:------|:------|  
|[!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] SP4 Enterprise|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] SP4 Developer|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer|  
|[!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] SP4 Standard|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] SP4 Small Business|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] SP4 Web|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web|  
|[!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] SP4 Workgroup|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] SP4 Express |[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Express|  
|[!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)] SP3 Datacenter|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)] SP3 Enterprise|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)] SP3 Developer|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer|  
|[!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)] SP3 Small Business|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)] SP3 Standard|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)] SP3 Web|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web|  
|[!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)] SP3 Workgroup|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[ssKilimanjaro](../../includes/sskilimanjaro-md.md)] SP3 Express |[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Express|  
|[!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] SP2 Enterprise|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] SP2 Developer|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] SP2 Standard|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] SP1 Web|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web|  
|[!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] SP2 Express |[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Express <br/> <br/> |  
|[!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] SP2 Business Intelligence|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] SP2 Evaluation|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Evaluation <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer|  
|[!INCLUDE[ssSQL14](../../includes/sssql14-md.md)] Enterprise|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[ssSQL14](../../includes/sssql14-md.md)] Developer|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[ssSQL14](../../includes/sssql14-md.md)] Standard|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[ssSQL14](../../includes/sssql14-md.md)] Web|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web|  
|[!INCLUDE[ssSQL14](../../includes/sssql14-md.md)] Express |[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Express <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer|  
|[!INCLUDE[ssSQL14](../../includes/sssql14-md.md)] Business Intelligence|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[ssSQL14](../../includes/sssql14-md.md)] Evaluation|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Evaluation <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer|
|[!INCLUDE[sssql16-md](../../includes/sssql16-md.md)] Enterprise|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[sssql16-md](../../includes/sssql16-md.md)] Developer|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[sssql16-md](../../includes/sssql16-md.md)] Standard|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[sssql16-md](../../includes/sssql16-md.md)] Web|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web|  
|[!INCLUDE[sssql16-md](../../includes/sssql16-md.md)] Express |[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Express <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer|  
|[!INCLUDE[sssql16-md](../../includes/sssql16-md.md)] Business Intelligence|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/> |  
|[!INCLUDE[sssql16-md](../../includes/sssql16-md.md)] Evaluation|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Evaluation <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer|
|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] release candidate* |[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise |  
|[!INCLUDE [sssql17-md](../../includes/sssql17-md.md)] Developer |[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise | 

 \* Microsoft support to upgrade from release candidate software is specifically for customers who participated in the Technology Adoption Program (TAP). 

   
###  <a name="SupportFor2005"></a> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Support for [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)]  
 This section discusses [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] support for [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)]. In [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)], you will be able to do the following:  
  
-   Attach a [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] database (mdf/ldf files) to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] instance of database engine.  
  
-   Restore a [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] database to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] instance of database engine from a backup.  
  
-   Back up a [!INCLUDE[ssASversion2005](../../includes/ssasversion2005-md.md)] cube and restore it on [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)].  
  
When a [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] database is upgraded to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)], the database compatibility level will be changed from 90 to 100. (In [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)], valid values for the database compatibility level are 100, 110, 120, 130, and 140.) [ALTER DATABASE Compatibility Level &#40;Transact-SQL&#41;](../../t-sql/statements/alter-database-transact-sql-compatibility-level.md) discusses how the compatibility level change could affect [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] applications.  
  
Any scenarios not specified in the list above are not supported, including but not limited to the following:  
  
- Installing [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] and [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] on same computer (side by side).  
  
- Using a [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] instance as a member of the replication topology that involves a [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] instance.  
  
- Configuring database mirroring between [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] and [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] instances.  
  
- Backing up the transaction log with log shipping between [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] and [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] instances.  
  
- Configuring linked servers between [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] and [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] instances.  
  
- Managing a [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] instance from a [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Management Studio.  
  
- Attaching a [!INCLUDE[ssASversion2005](../../includes/ssasversion2005-md.md)] cube in [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Management Studio.  
  
- Connecting to [!INCLUDE[ssISversion2005](../../includes/ssisversion2005-md.md)] from [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Management Studio.  
  
- Managing a [!INCLUDE[ssISversion2005](../../includes/ssisversion2005-md.md)] service from [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Management Studio.  
  
- Support for [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] third party custom Integration Services components, such as execute and upgrade.  
  
## [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Edition Upgrade  
The following table lists the supported edition upgrade scenarios in [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)].  
  
For step-by-step instructions on how to perform an edition upgrade, see [Upgrade to a Different Edition of SQL Server &#40;Setup&#41;](../../database-engine/install-windows/upgrade-to-a-different-edition-of-sql-server-setup.md).  
  
|Upgrade From|Upgrade To|  
|------------------|----------------|  
|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Server+CAL and Core)**|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise |  
|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Evaluation Enterprise**|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Server+CAL or Core License) <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> Upgrading from Evaluation (a free edition) to any of the paid editions is supported for stand-alone installations, but is not supported for clustered installations. This limitation does not apply to stand-alone instances installed on a Windows Failover Cluster participating in an availability group.|  
|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard**|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Server+CAL or Core License)|  
|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer**|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Server+CAL or Core License) <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Server+CAL or Core License) <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard|  
|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Express*|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Server+CAL or Core License) <br/><br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard <br/> <br/> [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Web|  
  
 Additionally you can also perform an edition upgrade between [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Server+CAL license) and [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Core License):  
  
|Edition Upgrade From|Edition Upgrade To|  
|--------------------------|------------------------|  
|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Server+CAL License)**|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Core License)|  
|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Core License)|[!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise (Server+CAL License)|  
  
 \* Also applies to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Express with Tools and [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Express with Advanced Services.  
  
 ** Changing the edition of a [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] failover cluster is limited. The following scenarios are not supported for [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] failover clusters:  
  
-   [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Enterprise to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer, Standard, or Evaluation.  
  
-   [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Developer to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard or Evaluation.  
  
-   [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Evaluation.  
  
-   [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Evaluation to [!INCLUDE[sssql17-md](../../includes/sssql17-md.md)] Standard.  
  
## See Also  

 [Editions and Supported Features for SQL Server 2017](../../sql-server/editions-and-components-of-sql-server-2017.md)
 
 [Hardware and Software Requirements for Installing SQL Server](../../sql-server/install/hardware-and-software-requirements-for-installing-sql-server.md)   
 
 [Upgrade SQL Server](../../database-engine/install-windows/upgrade-sql-server.md)  
  
