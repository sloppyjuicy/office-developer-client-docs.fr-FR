---
title: Append, méthode (Groupes ADOX)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f08b1bdbde8cc276e94947c2bd62250320f646c5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888586"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="31f9d-102">Append, méthode (Groupes ADOX)</span><span class="sxs-lookup"><span data-stu-id="31f9d-102">Append Method (ADOX Groups)</span></span>


<span data-ttu-id="31f9d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31f9d-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="31f9d-104">Ajoute un nouvel objet [Group](group-object-adox.md) à la collection [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="31f9d-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31f9d-105">Syntax</span></span>

<span data-ttu-id="31f9d-106">*Groupes*. Ajouter le*groupe*</span><span class="sxs-lookup"><span data-stu-id="31f9d-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="31f9d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31f9d-107">Parameters</span></span>

  - <span data-ttu-id="31f9d-108">*Group*</span><span class="sxs-lookup"><span data-stu-id="31f9d-108">*Group*</span></span>

  - <span data-ttu-id="31f9d-109">Objet **Group** à ajouter ou nom du groupe à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="31f9d-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="31f9d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="31f9d-110">Remarks</span></span>

<span data-ttu-id="31f9d-p101">La collection **Groups** d'un objet [Catalog](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un objet [User](user-object-adox.md) contient uniquement le groupe auquel l'utilisateur appartient.</span><span class="sxs-lookup"><span data-stu-id="31f9d-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="31f9d-113">Une erreur se produit si le fournisseur ne prend pas en charge la création de groupes.</span><span class="sxs-lookup"><span data-stu-id="31f9d-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <span data-ttu-id="31f9d-114">[!REMARQUE] Avant d'ajouter un objet **Group** à la collection **Groups** d'un objet **User**, un objet **Group** affecté de la même propriété [Name](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Groups** de l'objet **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="31f9d-114">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


