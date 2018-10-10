---
title: Users, collection (ADOX)
TOCTitle: Users Collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d68dc2dd368523e8ca3dd04a06008cea9bef337e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469550"
---
# <a name="users-collection-adox"></a><span data-ttu-id="72200-102">Users, collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="72200-102">Users Collection (ADOX)</span></span>


<span data-ttu-id="72200-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="72200-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72200-104">Contient tous les objets [User](user-object-adox.md) stockés d'un catalogue ou d'un groupe.</span><span class="sxs-lookup"><span data-stu-id="72200-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="72200-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="72200-105">Remarks</span></span>

<span data-ttu-id="72200-p101">La collection **Users** d'un [catalogue](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d'un [groupe](group-object-adox.md) représente uniquement les utilisateurs appartenant au groupe spécifique.</span><span class="sxs-lookup"><span data-stu-id="72200-p101">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="72200-p102">La méthode [Append](append-method-adox-users.md) d'une collection **Users** est unique pour ADOX. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="72200-p102">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="72200-110">Ajouter un nouvel utilisateur à la collection à l'aide de la méthode **Append**.</span><span class="sxs-lookup"><span data-stu-id="72200-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="72200-p103">Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="72200-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="72200-113">Accéder à un utilisateur de la collection à l'aide de la propriété [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="72200-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="72200-114">Renvoyer le nombre d'utilisateurs de la collection à l'aide de la propriété [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="72200-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="72200-115">Supprimer un utilisateur de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="72200-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="72200-116">Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="72200-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="72200-117">[!REMARQUE] Avant d'ajouter un objet <STRONG>User</STRONG> à la collection <STRONG>Users</STRONG> d'un objet <STRONG>Group</STRONG>, un objet <STRONG>User</STRONG> avec le même <A href="name-property-adox.md">nom</A> que celui à ajouter doit déjà exister dans la collection <STRONG>Users</STRONG> du <STRONG>catalogue</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="72200-117">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


