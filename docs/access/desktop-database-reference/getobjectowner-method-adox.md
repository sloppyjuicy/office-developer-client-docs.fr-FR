---
title: GetObjectOwner, méthode (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1a37b0f341c849358b649c2222df2955fd88f5d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927811"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="f698d-102">GetObjectOwner, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f698d-102">GetObjectOwner method (ADOX)</span></span>


<span data-ttu-id="f698d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f698d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f698d-104">Renvoie le propriétaire d'un objet dans un objet [Catalog](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="f698d-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f698d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f698d-105">Syntax</span></span>

<span data-ttu-id="f698d-106">*Propriétaire* = *catalogue*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="f698d-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="f698d-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f698d-107">Return value</span></span>

<span data-ttu-id="f698d-108">Renvoie une valeur de type **String** qui spécifie la propriété [Name](name-property-adox.md) de l'objet [User](user-object-adox.md) ou [Group](group-object-adox.md) qui détient l'objet.</span><span class="sxs-lookup"><span data-stu-id="f698d-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f698d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f698d-109">Parameters</span></span>

  - <span data-ttu-id="f698d-110">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="f698d-110">*ObjectName*</span></span>

  - <span data-ttu-id="f698d-111">Valeur de type **String** qui spécifie le nom de l'objet dont le propriétaire doit être renvoyé.</span><span class="sxs-lookup"><span data-stu-id="f698d-111">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="f698d-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="f698d-112">*ObjectType*</span></span>

  - <span data-ttu-id="f698d-113">Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="f698d-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="f698d-114">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="f698d-114">*ObjectTypeId*</span></span>

  - <span data-ttu-id="f698d-115">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f698d-115">Optional.</span></span> <span data-ttu-id="f698d-116">Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f698d-116">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="f698d-117">Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f698d-117">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f698d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f698d-118">Remarks</span></span>

<span data-ttu-id="f698d-119">Une erreur se produit si le fournisseur ne prend pas en charge le renvoi des propriétaires d'objets.</span><span class="sxs-lookup"><span data-stu-id="f698d-119">An error will occur if the provider does not support returning object owners.</span></span>

