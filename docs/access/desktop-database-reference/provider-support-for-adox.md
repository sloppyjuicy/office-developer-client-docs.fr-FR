---
title: Prise en charge du fournisseur pour ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a92ffe9b4b713518330d9dbfd9979d904a5abe8e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703509"
---
# <a name="provider-support-for-adox"></a>Prise en charge du fournisseur pour ADOX


**S’applique à**: Access 2013, Office 2013

Selon votre fournisseur de données OLE DB, certaines fonctionnalités d'ADOX ne sont pas prises en charge. ADOX est complètement pris en charge par le [fournisseur Microsoft OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Les fonctionnalités non prises en charge par le [fournisseur Microsoft OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md), le [fournisseur Microsoft OLE DB pour ODBC](microsoft-ole-db-provider-for-odbc.md) ou le [fournisseur Microsoft OLE DB pour Oracle](microsoft-ole-db-provider-for-oracle.md) sont répertoriées ci-dessous. ADOX n'est pas pris en charge par d'autres fournisseurs Microsoft OLE DB.

## <a name="microsoft-ole-db-provider-for-sql-server"></a>Fournisseur Microsoft OLE DB pour SQL Server

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objet ou collection</p></th>
<th><p>Restriction d'utilisation</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objet <strong>Catalog</strong></p></td>
<td><p>La méthode <strong>Create</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p>Collection <strong>Tables</strong></p></td>
<td><p>Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</p></td>
</tr>
<tr class="odd">
<td><p>Collection <strong>Views</strong></p></td>
<td><p>La collection <strong>Views</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedures</strong> , collection</p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Procedure</strong> , objet</p></td>
<td><p>La propriété <strong>Command</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Keys</strong> , collection</p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Users</strong> , collection</p></td>
<td><p>La collection <strong>Users</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Groups</strong> , collection</p></td>
<td><p>La collection <strong>Groups</strong> n'est pas prise en charge.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a>Fournisseur Microsoft OLE DB pour ODBC

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objet ou collection</p></th>
<th><p>Restriction d'utilisation</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objet <strong>Catalog</strong></p></td>
<td><p>La méthode <strong>Create</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tables</strong> , collection</p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.
 Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</p></td>
</tr>
<tr class="odd">
<td><p>Collection <strong>Procedures</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedure</strong> , objet</p></td>
<td><p>La propriété <strong>Command</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Indexes</strong> , collection</p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Keys</strong> , collection</p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Users</strong> , collection</p></td>
<td><p>La collection <strong>Users</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Groups</strong> , collection</p></td>
<td><p>La collection <strong>Groups</strong> n'est pas prise en charge.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a>Fournisseur Microsoft OLE DB pour Oracle

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objet ou collection</p></th>
<th><p>Restriction d'utilisation</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objet <strong>Catalog</strong></p></td>
<td><p>La méthode <strong>Create</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tables</strong> , collection</p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.
 Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</p></td>
</tr>
<tr class="odd">
<td><p>Collection <strong>Views</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="even">
<td><p>Objet <strong>View</strong></p></td>
<td><p>La propriété <strong>Command</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="odd">
<td><p>Collection <strong>Procedures</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedure</strong> , objet</p></td>
<td><p>La propriété <strong>Command</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Indexes</strong> , collection</p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Keys</strong> , collection</p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Users</strong> , collection</p></td>
<td><p>La collection <strong>Users</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>Groups</strong> , collection</p></td>
<td><p>La collection <strong>Groups</strong> n'est pas prise en charge.</p></td>
</tr>
</tbody>
</table>

