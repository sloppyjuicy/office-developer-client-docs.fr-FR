---
title: Groups, collection (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b75f6277695c00c251352e0ae2bdcc44f2c86d34
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929152"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="39fbd-102">Groups, collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="39fbd-102">Groups collection (ADOX)</span></span>


<span data-ttu-id="39fbd-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39fbd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39fbd-104">Contient tous les objets [Group](group-object-adox.md) stockés d'un catalogue ou d'un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39fbd-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="39fbd-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="39fbd-105">Remarks</span></span>

<span data-ttu-id="39fbd-p101">La collection **Groups** d'un [catalogue](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un [utilisateur](user-object-adox.md) représente le groupe auquel l'utilisateur appartient uniquement.</span><span class="sxs-lookup"><span data-stu-id="39fbd-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="39fbd-p102">La méthode [Append](append-method-adox-groups.md) d'une collection **Groups** est unique pour ADOX. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="39fbd-p102">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="39fbd-110">Ajouter un nouveau groupe de sécurité à la collection à l'aide de la méthode **Append**.</span><span class="sxs-lookup"><span data-stu-id="39fbd-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="39fbd-p103">Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="39fbd-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="39fbd-113">Accéder à un groupe de la collection à l'aide de la propriété [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="39fbd-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="39fbd-114">Renvoyer le nombre de groupes de la collection à l'aide de la propriété [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="39fbd-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="39fbd-115">Supprimer un groupe de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="39fbd-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="39fbd-116">Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="39fbd-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="39fbd-117">[!REMARQUE] Avant d'ajouter un objet <STRONG>Group</STRONG> à la collection <STRONG>Groups</STRONG> d'un objet <STRONG>User</STRONG>, un objet <STRONG>Group</STRONG> avec le même <A href="name-property-adox.md">nom</A> que celui à ajouter doit déjà exister dans la collection <STRONG>Groups</STRONG> du <STRONG>catalogue</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="39fbd-117">Before appending a <STRONG>Group</STRONG> object to the <STRONG>Groups</STRONG> collection of a <STRONG>User</STRONG> object, a <STRONG>Group</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Groups</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


