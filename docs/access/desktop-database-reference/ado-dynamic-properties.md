---
title: Propriétés dynamiques ADO
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fae0df2a4cc5c9de585d2b101e9fa31cb6a0a545
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714520"
---
# <a name="ado-dynamic-properties"></a>Propriétés dynamiques ADO

**S’applique à**: Access 2013, Office 2013

Des propriétés dynamiques peuvent être ajoutées aux collections [Properties](properties-collection-ado.md) des objets [Connection](connection-object-ado.md), [Command](command-object-ado.md) ou [Recordset](recordset-object-ado.md). La source de ces propriétés peut être un fournisseur de données, tel que le [fournisseur OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md) ou un fournisseur de services, tel que le [service de curseur Microsoft pour OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Consultez la documentation du fournisseur de données ou de services approprié pour plus d'informations sur une propriété dynamique spécifique.

L'[index de propriétés dynamiques ADO](ado-dynamic-property-index.md) fournit une référence croisée entre les noms ADO et OLE DB pour chaque propriété dynamique standard du fournisseur OLE DB.

Les propriétés dynamiques suivantes sont destinées à un emploi particulier ; elles sont également présentées dans les sources mentionnées précédemment. Les fonctionnalités spéciales fournies avec ADO sont présentées dans les rubriques d'aide d'ADO indiquées au bas de la page.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Propriété dynamique</th>
<th>Description</th>
</tr>
<tr class="odd">
<td><p><a href="optimize-property-dynamic-ado.md">Optimiser</a></p></td>
<td><p>Indique si un index doit être créé sur ce champ.</p></td>
</tr>
<tr class="even">
<td><p><a href="prompt-property-dynamic-ado.md">Prompt</a></p></td>
<td><p>Spécifie si le fournisseur OLE DB doit inviter l'utilisateur à fournir des informations d'initialisation.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Spécifie un nom pour l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Spécifie une chaîne de commande fournie par l'utilisateur, que la méthode <strong>Resync</strong> émet pour actualiser les données de la table nommée dans la propriété dynamique <strong>Unique Table</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></p></td>
<td><p><strong>Unique Table</strong> — Spécifie le nom de la table de base sur laquelle les mises à jour, des insertions et suppressions sont autorisées.<br/><br/><strong>Unique Schema</strong> : indique le schéma ou le nom du propriétaire de la table.<br/><br/><strong>Unique Catalog</strong> : indique le catalogue ou le nom de la base de données contenant la table.</p></td>
</tr>
<tr class="even">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a></p></td>
<td><p>Spécifie si la méthode <strong>UpdateBatch</strong> est suivie d'une opération de méthode <strong>Resync</strong> implicite et, si c'est le cas, la portée de cette opération.</p></td>
</tr>
</tbody>
</table>

<br/>

