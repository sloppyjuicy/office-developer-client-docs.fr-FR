---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b71d1f477435b4a9327b4156560d1aa2e6079536
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578702"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="eed1b-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="eed1b-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="eed1b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eed1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eed1b-105">Appelle une fonction interne pour vérifier que les applications clientes de paramètres transmis à MAPI et les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="eed1b-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eed1b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="eed1b-106">Header file:</span></span>  <br/> |<span data-ttu-id="eed1b-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="eed1b-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="eed1b-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="eed1b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eed1b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eed1b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eed1b-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="eed1b-110">Called by:</span></span>  <br/> |<span data-ttu-id="eed1b-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="eed1b-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="eed1b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eed1b-112">Parameters</span></span>

 <span data-ttu-id="eed1b-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="eed1b-113">_eMethod_</span></span>
  
> <span data-ttu-id="eed1b-114">[in] Spécifie, par l’énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="eed1b-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="eed1b-115">_Premier_</span><span class="sxs-lookup"><span data-stu-id="eed1b-115">_First_</span></span>
  
> <span data-ttu-id="eed1b-116">[in] Pointeur vers le premier argument dans la pile.</span><span class="sxs-lookup"><span data-stu-id="eed1b-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eed1b-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eed1b-117">Return value</span></span>

<span data-ttu-id="eed1b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="eed1b-118">S_OK</span></span> 
  
> <span data-ttu-id="eed1b-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="eed1b-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="eed1b-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="eed1b-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="eed1b-121">Une erreur a empêché l’opération de se terminer.</span><span class="sxs-lookup"><span data-stu-id="eed1b-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eed1b-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="eed1b-122">Remarks</span></span>

<span data-ttu-id="eed1b-123">Paramètres passés entre MAPI et service fournisseurs sont supposés être correct et sont soumis à la validation de débogage uniquement avec la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="eed1b-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="eed1b-124">Fournisseurs doivent vérifier tous les paramètres passés par les applications clientes, mais les clients doivent supposer que MAPI et le fournisseur de paramètres sont corrects.</span><span class="sxs-lookup"><span data-stu-id="eed1b-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="eed1b-125">Utilisez la macro **HR_FAILED** pour tester les valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="eed1b-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="eed1b-126">La macro **UlValidateParms** est appelée différemment selon que le code appelant est C ou C++.</span><span class="sxs-lookup"><span data-stu-id="eed1b-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="eed1b-127">Cette macro est utilisée pour valider les paramètres pour les quelques méthodes **IUnknown** et MAPI qui renvoient ULONG au lieu des valeurs HRESULT ; la macro [ValidateParms](validateparms.md) fonctionne pour tous les autres.</span><span class="sxs-lookup"><span data-stu-id="eed1b-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

