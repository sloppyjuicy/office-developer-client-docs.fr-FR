---
title: User, objet (référence à la base de données de bureau Access)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313159"
---
# <a name="user-object-adox"></a><span data-ttu-id="6fd40-102">User, objet (ADOX)</span><span class="sxs-lookup"><span data-stu-id="6fd40-102">User object (ADOX)</span></span>


<span data-ttu-id="6fd40-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fd40-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6fd40-104">Représente un compte d'utilisateur qui dispose d'autorisations d'accès à une base de données sécurisée.</span><span class="sxs-lookup"><span data-stu-id="6fd40-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fd40-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="6fd40-105">Remarks</span></span>

<span data-ttu-id="6fd40-p101">La collection [Users](users-collection-adox.md) d’un [catalogue](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d’un [groupe](group-object-adox.md) représente les utilisateurs du groupe spécifique uniquement.</span><span class="sxs-lookup"><span data-stu-id="6fd40-p101">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="6fd40-108">Avec les propriétés, collections et méthodes d'un objet **User**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="6fd40-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="6fd40-109">Identifier l’utilisateur à l’aide de la propriété [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6fd40-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="6fd40-110">Modifier le mot de passe d’un utilisateur à l’aide de la méthode [ChangePassword](changepassword-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6fd40-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="6fd40-111">Déterminer si un utilisateur dispose des autorisations de lecture, écriture ou suppression à l’aide des méthodes [GetPermissions](getpermissions-method-adox.md) et [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6fd40-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="6fd40-112">Accéder aux groupes auxquels un utilisateur appartient à l’aide de la collection [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6fd40-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="6fd40-113">Accéder aux propriétés spécifiques au fournisseur à l’aide de la collection [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6fd40-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

