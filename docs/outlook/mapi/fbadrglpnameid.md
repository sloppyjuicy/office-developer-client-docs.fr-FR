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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434829"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="d0375-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="d0375-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="d0375-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0375-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0375-105">Valide un tableau de structures qui décrivent les propriétés nommées et vérifie leur allocation.</span><span class="sxs-lookup"><span data-stu-id="d0375-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0375-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d0375-106">Header file:</span></span>  <br/> |<span data-ttu-id="d0375-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d0375-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d0375-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d0375-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d0375-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d0375-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d0375-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d0375-110">Called by:</span></span>  <br/> |<span data-ttu-id="d0375-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d0375-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="d0375-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0375-112">Parameters</span></span>

 <span data-ttu-id="d0375-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="d0375-113">_lppNameId_</span></span>
  
> <span data-ttu-id="d0375-114">dans Pointeur vers un tableau de structures [MAPINAMEID](mapinameid.md) décrivant les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="d0375-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="d0375-115">_Enregistrements CNAME_</span><span class="sxs-lookup"><span data-stu-id="d0375-115">_cNames_</span></span>
  
> <span data-ttu-id="d0375-116">dans Nombre de structures de propriété nommées dans le tableau vers lequel pointe le paramètre _lppNameId_ .</span><span class="sxs-lookup"><span data-stu-id="d0375-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d0375-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0375-117">Return value</span></span>

<span data-ttu-id="d0375-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="d0375-118">TRUE</span></span> 
  
> <span data-ttu-id="d0375-119">Une ou plusieurs des structures de nom de propriété spécifiées ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d0375-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="d0375-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="d0375-120">FALSE</span></span> 
  
> <span data-ttu-id="d0375-121">Les structures de nom de propriété spécifiées sont toutes valides.</span><span class="sxs-lookup"><span data-stu-id="d0375-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0375-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0375-122">Remarks</span></span>

<span data-ttu-id="d0375-123">La fonction **FBadRglpNameID** peut être utilisée lors de la configuration d'un appel à [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="d0375-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

