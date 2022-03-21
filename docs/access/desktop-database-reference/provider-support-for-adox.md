---
title: Prise en charge du fournisseur pour ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 635e76efa614ce02d72d6d521af0f21c7e50cca1
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631971"
---
# <a name="provider-support-for-adox"></a>Prise en charge du fournisseur pour ADOX


**S’applique à** : Access 2013, Office 2013

Selon votre fournisseur de données OLE DB, certaines fonctionnalités d'ADOX ne sont pas prises en charge. ADOX est complètement pris en charge par le [fournisseur Microsoft OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Les fonctionnalités non prises en charge par le [fournisseur Microsoft OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md), le [fournisseur Microsoft OLE DB pour ODBC](microsoft-ole-db-provider-for-odbc.md) ou le [fournisseur Microsoft OLE DB pour Oracle](microsoft-ole-db-provider-for-oracle.md) sont répertoriées ci-dessous. ADOX n'est pas pris en charge par d'autres fournisseurs Microsoft OLE DB.

## <a name="microsoft-ole-db-provider-for-sql-server"></a>Fournisseur Microsoft OLE DB pour SQL Server

<table>
<colgroup>
<col />
<col />
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
<td><p>Collection <strong>Procedures</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="odd">
<td><p>Objet <strong>Procedure</strong></p></td>
<td><p>La propriété <strong>Command</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p>Collection <strong>Keys</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="odd">
<td><p>Collection <strong>Users</strong></p></td>
<td><p>La collection <strong>Users</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p>Collection <strong>Groups</strong></p></td>
<td><p>La collection <strong>Groups</strong> n'est pas prise en charge.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a>Fournisseur Microsoft OLE DB pour ODBC

<table>
<colgroup>
<col />
<col />
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
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge. Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</p></td>
</tr>
<tr class="odd">
<td><p>Collection <strong>Procedures</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="even">
<td><p>Objet <strong>Procedure</strong></p></td>
<td><p>La propriété <strong>Command</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="odd">
<td><p>Collection  <strong>Indexes</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="even">
<td><p>Collection <strong>Keys</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="odd">
<td><p>Collection <strong>Users</strong></p></td>
<td><p>La collection <strong>Users</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p>Collection <strong>Groups</strong></p></td>
<td><p>La collection <strong>Groups</strong> n'est pas prise en charge.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a>Fournisseur Microsoft OLE DB pour Oracle

<table>
<colgroup>
<col />
<col />
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
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge. Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</p></td>
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
<td><p>Objet <strong>Procedure</strong></p></td>
<td><p>La propriété <strong>Command</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="odd">
<td><p>Collection  <strong>Indexes</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="even">
<td><p>Collection <strong>Keys</strong></p></td>
<td><p>Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</p></td>
</tr>
<tr class="odd">
<td><p>Collection <strong>Users</strong></p></td>
<td><p>La collection <strong>Users</strong> n'est pas prise en charge.</p></td>
</tr>
<tr class="even">
<td><p>Collection <strong>Groups</strong></p></td>
<td><p>La collection <strong>Groups</strong> n'est pas prise en charge.</p></td>
</tr>
</tbody>
</table>

