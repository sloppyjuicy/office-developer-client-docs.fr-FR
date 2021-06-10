---
title: GetObjectOwner, méthode (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 948464534f9bbfbea50c8eba2c926dea9cb9bcac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292257"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="7fdd4-102">GetObjectOwner, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7fdd4-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="7fdd4-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7fdd4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7fdd4-104">Renvoie le propriétaire d’un objet dans un objet [Catalog](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="7fdd4-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7fdd4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fdd4-105">Syntax</span></span>

<span data-ttu-id="7fdd4-106">*Propriétaire*  =  *Catalogue*. GetObjectOwner(*ObjectName*, *ObjectType* \[ ,*ObjectTypeId* \] )</span><span class="sxs-lookup"><span data-stu-id="7fdd4-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="7fdd4-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7fdd4-107">Return value</span></span>

<span data-ttu-id="7fdd4-108">Renvoie une valeur de type **String** qui spécifie la propriété [Name](name-property-adox.md) de l’objet [User](user-object-adox.md) ou [Group](group-object-adox.md) qui détient l’objet.</span><span class="sxs-lookup"><span data-stu-id="7fdd4-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fdd4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fdd4-109">Parameters</span></span>

|<span data-ttu-id="7fdd4-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7fdd4-110">Parameter</span></span>|<span data-ttu-id="7fdd4-111">Description</span><span class="sxs-lookup"><span data-stu-id="7fdd4-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7fdd4-112">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="7fdd4-112">*ObjectName*</span></span> |<span data-ttu-id="7fdd4-113">Valeur de type **String** qui spécifie le nom de l'objet dont le propriétaire doit être renvoyé.</span><span class="sxs-lookup"><span data-stu-id="7fdd4-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="7fdd4-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="7fdd4-114">*ObjectType*</span></span> |<span data-ttu-id="7fdd4-115">Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="7fdd4-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="7fdd4-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="7fdd4-116">*ObjectTypeId*</span></span> |<span data-ttu-id="7fdd4-p101">Facultatif. Valeur de type **Variant** qui spécifie le GUID d'un type d'objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. Sinon, il n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7fdd4-p101">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7fdd4-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="7fdd4-120">Remarks</span></span>

<span data-ttu-id="7fdd4-121">Une erreur se produit si le fournisseur ne prend pas en charge le renvoi des propriétaires d'objets.</span><span class="sxs-lookup"><span data-stu-id="7fdd4-121">An error will occur if the provider does not support returning object owners.</span></span>

