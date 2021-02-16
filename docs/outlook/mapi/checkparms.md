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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422277"
---
# <a name="checkparms"></a><span data-ttu-id="174f0-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="174f0-103">CheckParms</span></span>

  
  
<span data-ttu-id="174f0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="174f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="174f0-105">Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de services appelées par MAPI.</span><span class="sxs-lookup"><span data-stu-id="174f0-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="174f0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="174f0-106">Header file:</span></span>  <br/> |<span data-ttu-id="174f0-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="174f0-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="174f0-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="174f0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="174f0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="174f0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="174f0-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="174f0-110">Called by:</span></span>  <br/> |<span data-ttu-id="174f0-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="174f0-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="174f0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="174f0-112">Parameters</span></span>

 <span data-ttu-id="174f0-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="174f0-113">_eMethod_</span></span>
  
> <span data-ttu-id="174f0-114">[in] Spécifie, par l’éumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="174f0-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="174f0-115">_First_</span><span class="sxs-lookup"><span data-stu-id="174f0-115">_First_</span></span>
  
> <span data-ttu-id="174f0-116">[in] Pointeur vers le premier argument de la pile.</span><span class="sxs-lookup"><span data-stu-id="174f0-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="174f0-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="174f0-117">Return value</span></span>

<span data-ttu-id="174f0-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="174f0-118">S_OK</span></span> 
  
> <span data-ttu-id="174f0-119">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="174f0-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="174f0-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="174f0-120">Remarks</span></span>

<span data-ttu-id="174f0-121">Contrairement aux [macros ValidateParms](validateparms.md) et [UlValidateParms,](ulvalidateparms.md) la macro **CheckParms** n’effectue pas de validation de paramètre complète.</span><span class="sxs-lookup"><span data-stu-id="174f0-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="174f0-122">Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés être corrects, de sorte que **CheckParms** effectue une validation de débogage uniquement.</span><span class="sxs-lookup"><span data-stu-id="174f0-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

