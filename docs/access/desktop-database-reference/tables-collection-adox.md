---
title: Tables, collection (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716170"
---
# <a name="tables-collection-adox"></a><span data-ttu-id="f82f2-102">Tables, collection (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f82f2-102">Tables collection (ADOX)</span></span>


<span data-ttu-id="f82f2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f82f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f82f2-104">Contient tous les objets [Table](table-object-adox.md) d'un catalogue.</span><span class="sxs-lookup"><span data-stu-id="f82f2-104">Contains all [Table](table-object-adox.md) objects of a catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="f82f2-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f82f2-105">Remarks</span></span>

<span data-ttu-id="f82f2-p101">La méthode [Append](append-method-adox-tables.md) d'une collection **Tables** est unique pour ADOX. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="f82f2-p101">The [Append](append-method-adox-tables.md) method for a **Tables** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="f82f2-108">Ajouter une nouvelle table à la collection à l'aide de la méthode **Append**.</span><span class="sxs-lookup"><span data-stu-id="f82f2-108">Add a new table to the collection with the **Append** method.</span></span>

<span data-ttu-id="f82f2-p102">Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="f82f2-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="f82f2-111">Accéder à une table de la collection à l'aide de la propriété [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f82f2-111">Access a table in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="f82f2-112">Renvoyer le nombre de tables de la collection à l'aide de la propriété [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f82f2-112">Return the number of tables contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="f82f2-113">Supprimer une table de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="f82f2-113">Remove a table from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="f82f2-114">Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f82f2-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

<span data-ttu-id="f82f2-p103">Certains fournisseurs peuvent renvoyer d'autres objets de schéma, comme View, dans la collection Tables. Par conséquent, certaines collections ADOX peuvent contenir des références au même objet. En cas de suppression de l'objet d'une collection, la modification apportée ne sera pas visible dans une autre collection qui référence l'objet supprimé tant que vous n'avez pas invoqué la méthode Refresh sur la collection. Par exemple, avec le fournisseur OLE DB Provider for Microsoft Jet, des vues sont renvoyées avec la collection Tables. Si vous en supprimez une, vous devez actualiser la collection Tables pour qu'elle reflète la modification.</span><span class="sxs-lookup"><span data-stu-id="f82f2-p103">Some providers may return other schema objects, such as a View, in the Tables collection. Therefore, some ADOX collections may contain references to the same object. Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection. For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection. If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span></span>

