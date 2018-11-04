---
title: Append, méthode (Groupes ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d552539b84972b4a20fe0bff39b6c8570719bcf7
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950159"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="60569-102">Append, méthode (Groupes ADOX)</span><span class="sxs-lookup"><span data-stu-id="60569-102">Append method (ADOX Groups)</span></span>

<span data-ttu-id="60569-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60569-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60569-104">Ajoute un nouvel objet [Group](group-object-adox.md) à la collection [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="60569-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="60569-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60569-105">Syntax</span></span>

<span data-ttu-id="60569-106">*Groupes*. Ajouter le*groupe*</span><span class="sxs-lookup"><span data-stu-id="60569-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="60569-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60569-107">Parameters</span></span>

|<span data-ttu-id="60569-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="60569-108">Parameter</span></span>|<span data-ttu-id="60569-109">Description</span><span class="sxs-lookup"><span data-stu-id="60569-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="60569-110">*Group*</span><span class="sxs-lookup"><span data-stu-id="60569-110">*Group*</span></span> |<span data-ttu-id="60569-111">Objet **Group** à ajouter ou nom du groupe à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="60569-111">The **Group** object to append or the name of the group to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="60569-112">Notes</span><span class="sxs-lookup"><span data-stu-id="60569-112">Remarks</span></span>

<span data-ttu-id="60569-p101">La collection **Groups** d'un objet [Catalog](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un objet [User](user-object-adox.md) contient uniquement le groupe auquel l'utilisateur appartient.</span><span class="sxs-lookup"><span data-stu-id="60569-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="60569-115">Une erreur se produit si le fournisseur ne prend pas en charge la création de groupes.</span><span class="sxs-lookup"><span data-stu-id="60569-115">An error will occur if the provider does not support creating groups.</span></span>

> [!NOTE]
> <span data-ttu-id="60569-116">[!REMARQUE] Avant d'ajouter un objet **Group** à la collection **Groups** d'un objet **User**, un objet **Group** affecté de la même propriété [Name](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Groups** de l'objet **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="60569-116">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


