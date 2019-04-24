---
title: Group, objet (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e010ac58ff0b573d42c562ce3be7a99acab5abea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292117"
---
# <a name="group-object-adox"></a><span data-ttu-id="71c66-102">Group, objet (ADOX)</span><span class="sxs-lookup"><span data-stu-id="71c66-102">Group object (ADOX)</span></span>


<span data-ttu-id="71c66-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71c66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71c66-104">Représente un compte de groupe disposant des autorisations d'accès à une base de données sécurisée.</span><span class="sxs-lookup"><span data-stu-id="71c66-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="71c66-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="71c66-105">Remarks</span></span>

<span data-ttu-id="71c66-p101">La collection [Groups](groups-collection-adox.md) d'un [catalogue](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un [utilisateur](user-object-adox.md) représente le groupe auquel l'utilisateur appartient uniquement.</span><span class="sxs-lookup"><span data-stu-id="71c66-p101">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="71c66-108">Avec les propriétés, collections et méthodes d'un objet **Group**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="71c66-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="71c66-109">Identifier le groupe à l'aide de la propriété [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="71c66-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="71c66-110">Déterminer si un groupe dispose des autorisations de lecture, écriture ou suppression à l'aide des méthodes [GetPermissions](getpermissions-method-adox.md) et [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="71c66-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="71c66-111">Accéder aux comptes d'utilisateurs appartenant au groupe à l'aide de la collection [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="71c66-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="71c66-112">Accéder aux propriétés spécifiques au fournisseur à l’aide de la collection [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="71c66-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

