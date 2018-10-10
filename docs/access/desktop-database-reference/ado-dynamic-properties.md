---
title: Propriétés dynamiques ADO
TOCTitle: ADO Dynamic Properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a953157e7b38aab7989b4c52f60bfffd1c56766
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470832"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="0f655-102">Propriétés dynamiques ADO</span><span class="sxs-lookup"><span data-stu-id="0f655-102">ADO Dynamic Properties</span></span>


<span data-ttu-id="0f655-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f655-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0f655-p101">Des propriétés dynamiques peuvent être ajoutées aux collections [Properties](properties-collection-ado.md) des objets [Connection](connection-object-ado.md), [Command](command-object-ado.md) ou [Recordset](recordset-object-ado.md). La source de ces propriétés peut être un fournisseur de données, tel que le [fournisseur OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md) ou un fournisseur de services, tel que le [service de curseur Microsoft pour OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Consultez la documentation du fournisseur de données ou de services approprié pour plus d'informations sur une propriété dynamique spécifique.</span><span class="sxs-lookup"><span data-stu-id="0f655-p101">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects. The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="0f655-107">L'[index de propriétés dynamiques ADO](ado-dynamic-property-index.md) fournit une référence croisée entre les noms ADO et OLE DB pour chaque propriété dynamique standard du fournisseur OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0f655-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="0f655-p102">Les propriétés dynamiques suivantes sont destinées à un emploi particulier ; elles sont également présentées dans les sources mentionnées précédemment. Les fonctionnalités spéciales fournies avec ADO sont présentées dans les rubriques d'aide d'ADO indiquées au bas de la page.</span><span class="sxs-lookup"><span data-stu-id="0f655-p102">The following dynamic properties are of special interest, and are also documented in the sources mentioned above. Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f655-110"><a href="optimize-property-dynamic-ado.md">Optimiser</a></span><span class="sxs-lookup"><span data-stu-id="0f655-110"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="0f655-111">Indique si un index doit être créé sur ce champ.</span><span class="sxs-lookup"><span data-stu-id="0f655-111">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f655-112"><a href="prompt-property-dynamic-ado.md">Prompt</a></span><span class="sxs-lookup"><span data-stu-id="0f655-112"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="0f655-113">Spécifie si le fournisseur OLE DB doit inviter l'utilisateur à fournir des informations d'initialisation.</span><span class="sxs-lookup"><span data-stu-id="0f655-113">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f655-114"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="0f655-114"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="0f655-115">Spécifie un nom pour l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f655-115">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f655-116"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="0f655-116"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="0f655-117">Spécifie une chaîne de commande fournie par l'utilisateur, que la méthode <strong>Resync</strong> émet pour actualiser les données de la table nommée dans la propriété dynamique <strong>Unique Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f655-117">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f655-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="0f655-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="0f655-119"><strong>Unique Table</strong> — Spécifie le nom de la table de base sur laquelle les mises à jour, des insertions et suppressions sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="0f655-119"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span> <span data-ttu-id="0f655-120"><strong>Unique Schema</strong> : indique le schéma ou le nom du propriétaire de la table.</span><span class="sxs-lookup"><span data-stu-id="0f655-120"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span> <span data-ttu-id="0f655-121"><strong>Unique Catalog</strong> : indique le catalogue ou le nom de la base de données contenant la table.</span><span class="sxs-lookup"><span data-stu-id="0f655-121"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f655-122"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span><span class="sxs-lookup"><span data-stu-id="0f655-122"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="0f655-123">Spécifie si la méthode <strong>UpdateBatch</strong> est suivie d'une opération de méthode <strong>Resync</strong> implicite et, si c'est le cas, la portée de cette opération.</span><span class="sxs-lookup"><span data-stu-id="0f655-123">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

