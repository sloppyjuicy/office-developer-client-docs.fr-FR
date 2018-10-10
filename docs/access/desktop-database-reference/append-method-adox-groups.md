---
title: Append, méthode (Groupes ADOX)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c602896a629881d06a3f3cf80326e02340186e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472133"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="0a8df-102">Append, méthode (Groupes ADOX)</span><span class="sxs-lookup"><span data-stu-id="0a8df-102">Append Method (ADOX Groups)</span></span>


<span data-ttu-id="0a8df-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a8df-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="0a8df-104">Ajoute un nouvel objet [Group](group-object-adox.md) à la collection [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0a8df-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a8df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a8df-105">Syntax</span></span>

<span data-ttu-id="0a8df-106">*Groupes*. Ajouter le*groupe*</span><span class="sxs-lookup"><span data-stu-id="0a8df-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="0a8df-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a8df-107">Parameters</span></span>

  - <span data-ttu-id="0a8df-108">*Group*</span><span class="sxs-lookup"><span data-stu-id="0a8df-108">*Group*</span></span>

  - <span data-ttu-id="0a8df-109">Objet **Group** à ajouter ou nom du groupe à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="0a8df-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a8df-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0a8df-110">Remarks</span></span>

<span data-ttu-id="0a8df-p101">La collection **Groups** d'un objet [Catalog](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un objet [User](user-object-adox.md) contient uniquement le groupe auquel l'utilisateur appartient.</span><span class="sxs-lookup"><span data-stu-id="0a8df-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="0a8df-113">Une erreur se produit si le fournisseur ne prend pas en charge la création de groupes.</span><span class="sxs-lookup"><span data-stu-id="0a8df-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0a8df-114">[!REMARQUE] Avant d'ajouter un objet <STRONG>Group</STRONG> à la collection <STRONG>Groups</STRONG> d'un objet <STRONG>User</STRONG>, un objet <STRONG>Group</STRONG> affecté de la même propriété <A href="name-property-adox.md">Name</A> que celui à ajouter doit déjà exister dans la collection <STRONG>Groups</STRONG> de l'objet <STRONG>Catalog</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0a8df-114">Before appending a <STRONG>Group</STRONG> object to the <STRONG>Groups</STRONG> collection of a <STRONG>User</STRONG> object, a <STRONG>Group</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Groups</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


