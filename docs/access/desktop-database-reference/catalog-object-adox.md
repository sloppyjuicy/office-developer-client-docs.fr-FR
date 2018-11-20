---
title: Catalog, objet (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d680c89f7188dafd216edf62bd07c80fa924a119
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026238"
---
# <a name="catalog-object-adox"></a><span data-ttu-id="ccb02-102">Catalog, objet (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ccb02-102">Catalog object (ADOX)</span></span>


<span data-ttu-id="ccb02-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ccb02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ccb02-104">Contient des collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) et [Procedures](procedures-collection-adox.md)) qui décrivent le catalogue de schémas d'une source de données.</span><span class="sxs-lookup"><span data-stu-id="ccb02-104">Contains collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md), and [Procedures](procedures-collection-adox.md)) that describe the schema catalog of a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccb02-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ccb02-105">Remarks</span></span>

<span data-ttu-id="ccb02-p101">Vous pouvez modifier l'objet **Catalog** en ajoutant ou supprimant des objets, ou en modifiant des objets existants. Certains fournisseurs ne prennent pas en charge tous les objets du **catalogue** ou prennent en charge uniquement les informations de schémas d'affichage.</span><span class="sxs-lookup"><span data-stu-id="ccb02-p101">You can modify the **Catalog** object by adding or removing objects or by modifying existing objects. Some providers may not support all of the **Catalog** objects or may support only viewing schema information.</span></span>

<span data-ttu-id="ccb02-108">Avec les propriétés et méthodes d'un objet **Catalog**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="ccb02-108">With the properties and methods of a **Catalog** object, you can:</span></span>

- <span data-ttu-id="ccb02-109">Ouvrir le catalogue en définissant la propriété [ActiveConnection](activeconnection-property-adox.md) sur un objet [Connection](connection-object-ado.md) ADO ou une chaîne de connexion valide.</span><span class="sxs-lookup"><span data-stu-id="ccb02-109">Open the catalog by setting the [ActiveConnection](activeconnection-property-adox.md) property to an ADO [Connection](connection-object-ado.md) object or a valid connection string.</span></span>

- <span data-ttu-id="ccb02-110">Créer un nouveau catalogue à l'aide de la méthode [Create](create-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="ccb02-110">Create a new catalog with the [Create](create-method-adox.md) method.</span></span>

- <span data-ttu-id="ccb02-111">Identifier les propriétaires des objets dans un **catalogue** à l'aide des méthodes [GetObjectOwner](getobjectowner-method-adox.md) et [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox).</span><span class="sxs-lookup"><span data-stu-id="ccb02-111">Determine the owners of the objects in a **Catalog** with the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) methods.</span></span>

