---
title: Append, méthode (Utilisateurs ADOX)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8bce151e800b58e9c99c6dd6591114c53208a5c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469886"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="d5f23-102">Append, méthode (Utilisateurs ADOX)</span><span class="sxs-lookup"><span data-stu-id="d5f23-102">Append Method (ADOX Users)</span></span>


<span data-ttu-id="d5f23-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5f23-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="d5f23-104">Ajoute un nouvel objet [User](user-object-adox.md) à la collection [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d5f23-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f23-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5f23-105">Syntax</span></span>

<span data-ttu-id="d5f23-106">*Les utilisateurs*. Ajouter*l’utilisateur*\[,*le mot de passe*\]</span><span class="sxs-lookup"><span data-stu-id="d5f23-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="d5f23-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5f23-107">Parameters</span></span>

  - <span data-ttu-id="d5f23-108">*User*</span><span class="sxs-lookup"><span data-stu-id="d5f23-108">*User*</span></span>

  - <span data-ttu-id="d5f23-109">Valeur de type **Variant** qui contient l'objet **User** à ajouter ou le nom de l'utilisateur à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="d5f23-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="d5f23-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="d5f23-110">*Password*</span></span>

  - <span data-ttu-id="d5f23-111">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d5f23-111">Optional.</span></span> <span data-ttu-id="d5f23-112">Valeur de type **String** qui contient le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5f23-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="d5f23-113">Le paramètre *Password* correspond à la valeur spécifiée par la méthode [ChangePassword](changepassword-method-adox.md) d’un objet **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="d5f23-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f23-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d5f23-114">Remarks</span></span>

<span data-ttu-id="d5f23-p102">La collection **Users** d'un objet [Catalog](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d'un objet [Group](group-object-adox.md) représente uniquement les utilisateurs qui appartiennent à ce groupe.</span><span class="sxs-lookup"><span data-stu-id="d5f23-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="d5f23-117">Une erreur se produit si le fournisseur ne prend pas en charge la création d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d5f23-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d5f23-118">[!REMARQUE] Avant d'ajouter un objet <STRONG>User</STRONG> à la collection <STRONG>Users</STRONG> d'un objet <STRONG>Group</STRONG>, un objet <STRONG>User</STRONG> affecté de la même propriété <A href="name-property-adox.md">Name</A> que celui à ajouter doit déjà exister dans la collection <STRONG>Users</STRONG> de l'objet <STRONG>Catalog</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d5f23-118">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


