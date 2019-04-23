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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281714"
---
# <a name="ado-dynamic-properties"></a>Propriétés dynamiques ADO

**S’applique à** : Access 2013, Office 2013

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
<th>Dynamic, propriété</th>
<th>Description</th>
</tr>
<tr class="odd">
<td><p><a href="optimize-property-dynamic-ado.md">Vos</a></p></td>
<td><p>Indique si un index doit être créé sur ce champ.</p></td>
</tr>
<tr class="even">
<td><p><a href="prompt-property-dynamic-ado.md">Prompt</a></p></td>
<td><p>Indique si le fournisseur OLE DB doit demander à l'utilisateur des informations d'initialisation.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Indique le nom de l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Spécifie une chaîne de commande fournie par l'utilisateur, que la méthode <strong>Resync</strong> émet pour actualiser les données de la table nommée dans la propriété dynamique <strong>Unique Table</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></p></td>
<td><p><strong>Unique table</strong> — spécifie le nom de la table de base dans laquelle les mises à jour, les insertions et les suppressions sont autorisées.<br/><br/><strong>Schéma unique</strong> : spécifie le schéma ou le nom du propriétaire de la table.<br/><br/><strong>Catalogue unique</strong> — spécifie le catalogue ou le nom de la base de données contenant la table.</p></td>
</tr>
<tr class="even">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a></p></td>
<td><p>Spécifie si la méthode <strong>UpdateBatch</strong> est suivie d'une opération de méthode <strong>Resync</strong> implicite et, si c'est le cas, la portée de cette opération.</p></td>
</tr>
</tbody>
</table>

<br/>

