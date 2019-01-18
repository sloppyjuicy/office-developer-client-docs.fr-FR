---
title: Append, méthode (Utilisateurs ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d05cf352515d8fe4faa868088c9ba9cc8a024145
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707597"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="b104e-102">Append, méthode (Utilisateurs ADOX)</span><span class="sxs-lookup"><span data-stu-id="b104e-102">Append method (ADOX Users)</span></span>

<span data-ttu-id="b104e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b104e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b104e-104">Ajoute un nouvel objet [User](user-object-adox.md) à la collection [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b104e-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b104e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b104e-105">Syntax</span></span>

<span data-ttu-id="b104e-106">*Les utilisateurs*. Ajouter*l’utilisateur*\[,*le mot de passe*\]</span><span class="sxs-lookup"><span data-stu-id="b104e-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="b104e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b104e-107">Parameters</span></span>

|<span data-ttu-id="b104e-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b104e-108">Parameter</span></span>|<span data-ttu-id="b104e-109">Description</span><span class="sxs-lookup"><span data-stu-id="b104e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b104e-110">*User*</span><span class="sxs-lookup"><span data-stu-id="b104e-110">*User*</span></span> |<span data-ttu-id="b104e-111">Valeur de type **Variant** qui contient l'objet **User** à ajouter ou le nom de l'utilisateur à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="b104e-111">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>|
|<span data-ttu-id="b104e-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="b104e-112">*Password*</span></span> |<span data-ttu-id="b104e-113">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="b104e-113">Optional.</span></span> <span data-ttu-id="b104e-114">Valeur de type **String** qui contient le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b104e-114">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="b104e-115">Le paramètre *Password* correspond à la valeur spécifiée par la méthode [ChangePassword](changepassword-method-adox.md) d’un objet **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="b104e-115">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b104e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b104e-116">Remarks</span></span>

<span data-ttu-id="b104e-p102">La collection **Users** d'un objet [Catalog](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d'un objet [Group](group-object-adox.md) représente uniquement les utilisateurs qui appartiennent à ce groupe.</span><span class="sxs-lookup"><span data-stu-id="b104e-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="b104e-119">Une erreur se produit si le fournisseur ne prend pas en charge la création d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b104e-119">An error will occur if the provider does not support creating users.</span></span>

> [!NOTE]
> <span data-ttu-id="b104e-120">[!REMARQUE] Avant d'ajouter un objet **User** à la collection **Users** d'un objet **Group**, un objet **User** affecté de la même propriété [Name](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Users** de l'objet **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="b104e-120">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


