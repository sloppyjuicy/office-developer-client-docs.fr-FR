---
title: GetObjectOwner, méthode (ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e6c2432370f2480484cf1165249bc8573b27372
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603111"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="23262-102">GetObjectOwner, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="23262-102">GetObjectOwner Method (ADOX)</span></span>


<span data-ttu-id="23262-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="23262-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="23262-104">Renvoie le propriétaire d'un objet dans un objet [Catalog](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="23262-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="23262-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23262-105">Syntax</span></span>

<span data-ttu-id="23262-106">*Propriétaire* = *catalogue*. GetObjectOwner (*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="23262-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

<span data-ttu-id="23262-107"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="23262-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="23262-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="23262-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="23262-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="23262-109">Return value</span></span>
>>>>>>> <span data-ttu-id="23262-110">master</span><span class="sxs-lookup"><span data-stu-id="23262-110">master</span></span>

<span data-ttu-id="23262-111">Renvoie une valeur de type **String** qui spécifie la propriété [Name](name-property-adox.md) de l'objet [User](user-object-adox.md) ou [Group](group-object-adox.md) qui détient l'objet.</span><span class="sxs-lookup"><span data-stu-id="23262-111">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="23262-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23262-112">Parameters</span></span>

  - <span data-ttu-id="23262-113">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="23262-113">*ObjectName*</span></span>

  - <span data-ttu-id="23262-114">Valeur de type **String** qui spécifie le nom de l'objet dont le propriétaire doit être renvoyé.</span><span class="sxs-lookup"><span data-stu-id="23262-114">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="23262-115">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="23262-115">*ObjectType*</span></span>

  - <span data-ttu-id="23262-116">Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="23262-116">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="23262-117">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="23262-117">*ObjectTypeId*</span></span>

  - <span data-ttu-id="23262-118">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="23262-118">Optional.</span></span> <span data-ttu-id="23262-119">Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB.</span><span class="sxs-lookup"><span data-stu-id="23262-119">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="23262-120">Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="23262-120">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="23262-121">Notes</span><span class="sxs-lookup"><span data-stu-id="23262-121">Remarks</span></span>

<span data-ttu-id="23262-122">Une erreur se produit si le fournisseur ne prend pas en charge le renvoi des propriétaires d'objets.</span><span class="sxs-lookup"><span data-stu-id="23262-122">An error will occur if the provider does not support returning object owners.</span></span>

