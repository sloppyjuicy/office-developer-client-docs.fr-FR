---
title: Unique Table, Unique Schema, Unique Catalog, propriétés dynamiques (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f4bf93afc200edd88e89cf5d4e90435c2476942
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721352"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a><span data-ttu-id="daeb3-102">Unique Table, Unique Schema, Unique Catalog, propriétés dynamiques (ADO)</span><span class="sxs-lookup"><span data-stu-id="daeb3-102">Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)</span></span>


<span data-ttu-id="daeb3-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="daeb3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="daeb3-104">Permet de contrôler précisément les modifications apportées à une table de base déterminée dans un objet [Recordset](recordset-object-ado.md) formé par une opération JOIN dans plusieurs tables de base.</span><span class="sxs-lookup"><span data-stu-id="daeb3-104">Enables you to closely control modifications to a particular base table in a [Recordset](recordset-object-ado.md) that was formed by a JOIN operation on multiple base tables.</span></span>

  - <span data-ttu-id="daeb3-105">La propriété **Unique Table** spécifie le nom de la table de base dans laquelle les mises à jour, les insertions et les suppressions sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="daeb3-105">**Unique Table** specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span>

  - <span data-ttu-id="daeb3-106">La propriété **Unique Schema** spécifie le *schéma* ou le nom du propriétaire de la table.</span><span class="sxs-lookup"><span data-stu-id="daeb3-106">**Unique Schema** specifies the *schema*, or name of the owner of the table.</span></span>

  - <span data-ttu-id="daeb3-107">La propriété **Unique Catalog** spécifie le *catalogue* ou le nom de la base de données contenant la table.</span><span class="sxs-lookup"><span data-stu-id="daeb3-107">**Unique Catalog** specifies the *catalog*, or name of the database containing the table.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="daeb3-108">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="daeb3-108">Settings and return values</span></span>

<span data-ttu-id="daeb3-109">Définit ou renvoie une valeur de type **String** qui représente le nom d'une table, d'un schéma ou d'un catalogue.</span><span class="sxs-lookup"><span data-stu-id="daeb3-109">Sets or returns a **String** value that is the name of a table, schema, or catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="daeb3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="daeb3-110">Remarks</span></span>

<span data-ttu-id="daeb3-p101">La table de base souhaitée est identifiée de manière unique par le nom de son catalogue, de son schéma et de sa table. Lorsque la propriété **Unique Table** est définie, les valeurs des propriétés **Unique Schema** ou **Unique Catalog** sont utilisées pour rechercher la table de base. Il est prévu, mais pas obligatoire, que l'une ou les deux propriétés **Unique Schema** et **Unique Catalog** soient définies avant la propriété **Unique Table**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-p101">The desired base table is uniquely identified by its catalog, schema, and table names. When the **Unique Table** property is set, the values of the **Unique Schema** or **Unique Catalog** properties are used to find the base table. It is intended, but not required, that either or both the **Unique Schema** and **Unique Catalog** properties be set before the **Unique Table** property is set.</span></span>

<span data-ttu-id="daeb3-p102">La clé primaire de la propriété **Unique Table** est considérée comme la clé primaire de l'ensemble du **Recordset**. Il s'agit de la clé utilisée pour toutes les méthodes nécessitant une clé primaire.</span><span class="sxs-lookup"><span data-stu-id="daeb3-p102">The primary key of the **Unique Table** is treated as the primary key of the entire **Recordset**. This is the key that is used for any method requiring a primary key.</span></span>

<span data-ttu-id="daeb3-p103">Lorsque la propriété **Unique Table** est définie, la méthode [Delete](delete-method-ado-recordset.md) n'affecte que la table nommée. Les méthodes [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md) et [UpdateBatch](updatebatch-method-ado.md) affectent toutes les tables de base sous-jacentes concernées de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-p103">While **Unique Table** is set, the [Delete](delete-method-ado-recordset.md) method affects only the named table. The [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md), and [UpdateBatch](updatebatch-method-ado.md) methods affect any appropriate underlying base tables of the **Recordset**.</span></span>

<span data-ttu-id="daeb3-p104">La propriété **Unique Table** doit être spécifiée avant d'effectuer des resynchronisations personnalisées. Si la propriété **Unique Table** n'a pas été spécifiée, la propriété [Resync Command](resync-command-property-dynamic-ado.md) n'a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="daeb3-p104">**Unique Table** must be specified before doing any custom resynchronizations. If **Unique Table** has not been specified, the [Resync Command](resync-command-property-dynamic-ado.md) property will have no effect.</span></span>

<span data-ttu-id="daeb3-120">Une erreur d'exécution est générée si aucune table de base unique n'est trouvée.</span><span class="sxs-lookup"><span data-stu-id="daeb3-120">A run-time error results if a unique base table cannot be found.</span></span>

<span data-ttu-id="daeb3-121">Ces propriétés dynamiques sont toutes ajoutées à la collection **Properties** de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-121">These dynamic properties are all appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

