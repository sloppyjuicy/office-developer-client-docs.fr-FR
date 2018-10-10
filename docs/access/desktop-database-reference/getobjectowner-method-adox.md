---
title: GetObjectOwner, méthode (ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e20141e379cb207819744fd65b78abf7d2d15712
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472136"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="c3188-102">GetObjectOwner, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c3188-102">GetObjectOwner Method (ADOX)</span></span>


<span data-ttu-id="c3188-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3188-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="c3188-104">Renvoie le propriétaire d'un objet dans un objet [Catalog](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="c3188-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3188-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3188-105">Syntax</span></span>

<span data-ttu-id="c3188-106">*Propriétaire* = *catalogue*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="c3188-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="c3188-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c3188-107">Return Value</span></span>

<span data-ttu-id="c3188-108">Renvoie une valeur de type **String** qui spécifie la propriété [Name](name-property-adox.md) de l'objet [User](user-object-adox.md) ou [Group](group-object-adox.md) qui détient l'objet.</span><span class="sxs-lookup"><span data-stu-id="c3188-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3188-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3188-109">Parameters</span></span>

  - <span data-ttu-id="c3188-110">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="c3188-110">*ObjectName*</span></span>

  - <span data-ttu-id="c3188-111">Valeur de type **String** qui spécifie le nom de l'objet dont le propriétaire doit être renvoyé.</span><span class="sxs-lookup"><span data-stu-id="c3188-111">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="c3188-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="c3188-112">*ObjectType*</span></span>

  - <span data-ttu-id="c3188-113">Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="c3188-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="c3188-114">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="c3188-114">*ObjectTypeId*</span></span>

  - <span data-ttu-id="c3188-115">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="c3188-115">Optional.</span></span> <span data-ttu-id="c3188-116">Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c3188-116">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="c3188-117">Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c3188-117">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3188-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c3188-118">Remarks</span></span>

<span data-ttu-id="c3188-119">Une erreur se produit si le fournisseur ne prend pas en charge le renvoi des propriétaires d'objets.</span><span class="sxs-lookup"><span data-stu-id="c3188-119">An error will occur if the provider does not support returning object owners.</span></span>

