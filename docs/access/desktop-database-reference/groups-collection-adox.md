---
title: Groups, collection (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21f1880a9effca6e51bc1e8b52a58dce22ce1ea9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292075"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="c5741-102">Groups, collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c5741-102">Groups collection (ADOX)</span></span>

<span data-ttu-id="c5741-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5741-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5741-104">Contient tous les objets [Group](group-object-adox.md) stockés d’un catalogue ou d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c5741-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5741-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5741-105">Remarks</span></span>

<span data-ttu-id="c5741-p101">La collection **Groups** d'un [catalogue](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un [utilisateur](user-object-adox.md) représente le groupe auquel l'utilisateur appartient uniquement.</span><span class="sxs-lookup"><span data-stu-id="c5741-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="c5741-p102">La méthode [Append](append-method-adox-groups.md) d'une collection **Groups** est unique pour ADOX. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c5741-p102">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX. You can:</span></span>

- <span data-ttu-id="c5741-110">Ajouter un nouveau groupe de sécurité à la collection à l'aide de la méthode **Append**.</span><span class="sxs-lookup"><span data-stu-id="c5741-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="c5741-p103">Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c5741-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

- <span data-ttu-id="c5741-113">Accéder à un groupe de la collection à l'aide de la propriété [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c5741-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="c5741-114">Renvoyer le nombre de groupes de la collection à l'aide de la propriété [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c5741-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="c5741-115">Supprimer un groupe de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="c5741-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="c5741-116">Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l’aide de la méthode [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c5741-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="c5741-117">[!REMARQUE] Avant d'ajouter un objet **Group** à la collection **Groups** d'un objet **User**, un objet **Group** avec le même [nom](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Groups** du **catalogue**.</span><span class="sxs-lookup"><span data-stu-id="c5741-117">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


