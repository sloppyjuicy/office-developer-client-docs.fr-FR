---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5732dd3c1587c127cf153ebcadd9b791e6abb9ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582034"
---
# <a name="checkparms"></a><span data-ttu-id="186f5-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="186f5-103">CheckParms</span></span>

  
  
<span data-ttu-id="186f5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="186f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="186f5-105">Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de service appelées par MAPI.</span><span class="sxs-lookup"><span data-stu-id="186f5-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="186f5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="186f5-106">Header file:</span></span>  <br/> |<span data-ttu-id="186f5-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="186f5-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="186f5-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="186f5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="186f5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="186f5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="186f5-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="186f5-110">Called by:</span></span>  <br/> |<span data-ttu-id="186f5-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="186f5-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="186f5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="186f5-112">Parameters</span></span>

 <span data-ttu-id="186f5-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="186f5-113">_eMethod_</span></span>
  
> <span data-ttu-id="186f5-114">[in] Spécifie, par l’énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="186f5-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="186f5-115">_Premier_</span><span class="sxs-lookup"><span data-stu-id="186f5-115">_First_</span></span>
  
> <span data-ttu-id="186f5-116">[in] Pointeur vers le premier argument dans la pile.</span><span class="sxs-lookup"><span data-stu-id="186f5-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="186f5-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="186f5-117">Return value</span></span>

<span data-ttu-id="186f5-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="186f5-118">S_OK</span></span> 
  
> <span data-ttu-id="186f5-119">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="186f5-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="186f5-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="186f5-120">Remarks</span></span>

<span data-ttu-id="186f5-121">Contrairement aux [ValidateParms](validateparms.md) et [UlValidateParms](ulvalidateparms.md) des macros, la macro **CheckParms** n’effectue pas une validation de paramètre complet.</span><span class="sxs-lookup"><span data-stu-id="186f5-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="186f5-122">Paramètres passés entre MAPI et service fournisseurs sont supposés soit correct **CheckParms** effectue une validation de débogage uniquement.</span><span class="sxs-lookup"><span data-stu-id="186f5-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

