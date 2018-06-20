---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3f04c5be240f63d35ea8dba0f7abbf1085f2a41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783280"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="a02ad-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="a02ad-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="a02ad-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a02ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a02ad-105">Valide un tableau de structures qui décrivent les propriétés nommées et vérifie leur affectation.</span><span class="sxs-lookup"><span data-stu-id="a02ad-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a02ad-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a02ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="a02ad-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="a02ad-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="a02ad-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a02ad-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a02ad-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a02ad-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a02ad-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="a02ad-110">Called by:</span></span>  <br/> |<span data-ttu-id="a02ad-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="a02ad-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="a02ad-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a02ad-112">Parameters</span></span>

 <span data-ttu-id="a02ad-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="a02ad-113">_lppNameId_</span></span>
  
> <span data-ttu-id="a02ad-114">[in] Pointeur vers un tableau de structures [MAPINAMEID](mapinameid.md) décrivant les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="a02ad-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="a02ad-115">_enregistrements CNAME_</span><span class="sxs-lookup"><span data-stu-id="a02ad-115">_cNames_</span></span>
  
> <span data-ttu-id="a02ad-116">[in] Nombre de structures de propriété nommée dans le tableau indiqué par le paramètre _lppNameId_ .</span><span class="sxs-lookup"><span data-stu-id="a02ad-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a02ad-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a02ad-117">Return value</span></span>

<span data-ttu-id="a02ad-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="a02ad-118">TRUE</span></span> 
  
> <span data-ttu-id="a02ad-119">Un ou plusieurs des structures de nom de propriété spécifié ne sont pas valide.</span><span class="sxs-lookup"><span data-stu-id="a02ad-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="a02ad-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="a02ad-120">FALSE</span></span> 
  
> <span data-ttu-id="a02ad-121">Les structures de nom de propriété spécifié sont valides.</span><span class="sxs-lookup"><span data-stu-id="a02ad-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a02ad-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="a02ad-122">Remarks</span></span>

<span data-ttu-id="a02ad-123">La fonction **FBadRglpNameID** peut être utilisée lorsque vous configurez pour un appel à [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="a02ad-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

