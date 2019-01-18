---
title: Users, collection (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 24d7a5cab3260dac80b39e5134938c5f55175851
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720407"
---
# <a name="users-collection-adox"></a><span data-ttu-id="78147-102">Users, collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="78147-102">Users collection (ADOX)</span></span>

<span data-ttu-id="78147-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78147-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78147-104">Contient tous les objets [User](user-object-adox.md) stockés d'un catalogue ou d'un groupe.</span><span class="sxs-lookup"><span data-stu-id="78147-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="78147-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="78147-105">Remarks</span></span>

<span data-ttu-id="78147-p101">La collection **Users** d'un [catalogue](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d'un [groupe](group-object-adox.md) représente uniquement les utilisateurs appartenant au groupe spécifique.</span><span class="sxs-lookup"><span data-stu-id="78147-p101">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="78147-p102">La méthode [Append](append-method-adox-users.md) d'une collection **Users** est unique pour ADOX. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="78147-p102">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX. You can:</span></span>

- <span data-ttu-id="78147-110">Ajouter un nouvel utilisateur à la collection à l'aide de la méthode **Append**.</span><span class="sxs-lookup"><span data-stu-id="78147-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="78147-p103">Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="78147-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

- <span data-ttu-id="78147-113">Accéder à un utilisateur de la collection à l'aide de la propriété [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="78147-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="78147-114">Renvoyer le nombre d'utilisateurs de la collection à l'aide de la propriété [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="78147-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="78147-115">Supprimer un utilisateur de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="78147-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="78147-116">Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="78147-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="78147-117">[!REMARQUE] Avant d'ajouter un objet **User** à la collection **Users** d'un objet **Group**, un objet **User** avec le même [nom](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Users** du **catalogue**.</span><span class="sxs-lookup"><span data-stu-id="78147-117">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>

