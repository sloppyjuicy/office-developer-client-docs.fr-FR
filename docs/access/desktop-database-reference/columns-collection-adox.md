---
title: Columns, collection (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13f9a17d7dfcd9e621e4f4b1f1fcc03e88b4d832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471900"
---
# <a name="columns-collection-adox"></a><span data-ttu-id="249bf-102">Columns, collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="249bf-102">Columns Collection (ADOX)</span></span>


<span data-ttu-id="249bf-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="249bf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="249bf-104">Contient tous les objets de [colonne](column-object-adox.md) d'une table, d'un index ou d'une clé.</span><span class="sxs-lookup"><span data-stu-id="249bf-104">Contains all [Column](column-object-adox.md) objects of a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="249bf-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="249bf-105">Remarks</span></span>

<span data-ttu-id="249bf-p101">La méthode [Append](append-method-adox-columns.md) d'une collection **Columns** est unique pour ADOX. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="249bf-p101">The [Append](append-method-adox-columns.md) method for a **Columns** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="249bf-108">Ajouter une nouvelle colonne à la collection à l'aide de la méthode **Append**.</span><span class="sxs-lookup"><span data-stu-id="249bf-108">Add a new column to the collection with the **Append** method.</span></span>

<span data-ttu-id="249bf-p102">Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="249bf-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="249bf-111">Accéder à une colonne de la collection à l'aide de la propriété [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="249bf-111">Access a column in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="249bf-112">Renvoyer le nombre de colonnes de la collection à l'aide de la propriété [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="249bf-112">Return the number of columns contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="249bf-113">Supprimer une colonne de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="249bf-113">Remove a column from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="249bf-114">Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="249bf-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="249bf-115">[!REMARQUE] Une erreur survient lors de l'ajout d'une <STRONG>colonne</STRONG> à la collection <STRONG>Columns</STRONG> d'un <A href="index-object-adox.md">index</A> si la <STRONG>colonne</STRONG> n'existe pas dans une <A href="table-object-adox.md">table</A> déjà ajoutée à la collection <A href="tables-collection-adox.md">Tables</A>.</span><span class="sxs-lookup"><span data-stu-id="249bf-115">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


