---
title: Columns, collection (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1827fe11696e28871bdd03594ff0d7057c377dc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720484"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="c1dde-102">Columns, collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c1dde-102">Columns collection (ADOX)</span></span>


<span data-ttu-id="c1dde-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1dde-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1dde-104">Contient tous les objets de [colonne](column-object-adox.md) d'une table, d'un index ou d'une clé.</span><span class="sxs-lookup"><span data-stu-id="c1dde-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1dde-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1dde-105">Remarks</span></span>

<span data-ttu-id="c1dde-p101">La méthode [Append](append-method-adox-columns.md) d'une collection **Columns** est unique pour ADOX. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1dde-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="c1dde-108">Ajouter une nouvelle colonne à la collection à l'aide de la méthode **Append**.</span><span class="sxs-lookup"><span data-stu-id="c1dde-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="c1dde-p102">Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c1dde-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="c1dde-111">Accéder à une colonne de la collection à l'aide de la propriété [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c1dde-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="c1dde-112">Renvoyer le nombre de colonnes de la collection à l'aide de la propriété [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c1dde-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="c1dde-113">Supprimer une colonne de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="c1dde-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="c1dde-114">Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c1dde-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="c1dde-115">[!REMARQUE] Une erreur survient lors de l'ajout d'une **colonne** à la collection **Columns** d'un [index](index-object-adox.md) si la **colonne** n'existe pas dans une [table](table-object-adox.md) déjà ajoutée à la collection [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="c1dde-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


