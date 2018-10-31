---
title: Columns, collection (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d49fa1bf77a66dbab829aff20ee666ae1a5082cc
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862215"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="e8540-102">Columns, collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e8540-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="e8540-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8540-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8540-104">Contient tous les objets de [colonne](column-object-adox.md) d'une table, d'un index ou d'une clé.</span><span class="sxs-lookup"><span data-stu-id="e8540-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8540-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8540-105">Remarks</span></span>

<span data-ttu-id="e8540-p101">La méthode [Append](append-method-adox-columns.md) d'une collection **Columns** est unique pour ADOX. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="e8540-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="e8540-108">Ajouter une nouvelle colonne à la collection à l'aide de la méthode **Append**.</span><span class="sxs-lookup"><span data-stu-id="e8540-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="e8540-p102">Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="e8540-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="e8540-111">Accéder à une colonne de la collection à l'aide de la propriété [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e8540-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="e8540-112">Renvoyer le nombre de colonnes de la collection à l'aide de la propriété [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e8540-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="e8540-113">Supprimer une colonne de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="e8540-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="e8540-114">Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e8540-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <span data-ttu-id="e8540-115">[!REMARQUE] Une erreur survient lors de l'ajout d'une **colonne** à la collection **Columns** d'un [index](index-object-adox.md) si la **colonne** n'existe pas dans une [table](table-object-adox.md) déjà ajoutée à la collection [Tables](tables-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e8540-115">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


