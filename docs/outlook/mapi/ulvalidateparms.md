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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360493"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="c4ec8-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="c4ec8-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="c4ec8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4ec8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4ec8-105">Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmises aux fournisseurs de services et MAPI.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4ec8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c4ec8-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4ec8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c4ec8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c4ec8-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c4ec8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4ec8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c4ec8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c4ec8-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c4ec8-110">Called by:</span></span>  <br/> |<span data-ttu-id="c4ec8-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="c4ec8-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="c4ec8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4ec8-112">Parameters</span></span>

 <span data-ttu-id="c4ec8-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="c4ec8-113">_eMethod_</span></span>
  
> <span data-ttu-id="c4ec8-114">dans Spécifie, par énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="c4ec8-115">_First_</span><span class="sxs-lookup"><span data-stu-id="c4ec8-115">_First_</span></span>
  
> <span data-ttu-id="c4ec8-116">dans Pointeur vers le premier argument de la pile.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4ec8-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c4ec8-117">Return value</span></span>

<span data-ttu-id="c4ec8-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4ec8-118">S_OK</span></span> 
  
> <span data-ttu-id="c4ec8-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c4ec8-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="c4ec8-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="c4ec8-121">Une erreur a empêché l'exécution de l'opération.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4ec8-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="c4ec8-122">Remarks</span></span>

<span data-ttu-id="c4ec8-123">Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés être corrects et soumis à la validation de débogage uniquement avec la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="c4ec8-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="c4ec8-124">Les fournisseurs doivent vérifier tous les paramètres transmis par les applications clientes, mais les clients doivent supposer que les paramètres MAPI et de fournisseur sont corrects.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="c4ec8-125">Utilisez la macro **HR_FAILED** pour tester les valeurs renvoyées.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="c4ec8-126">La macro **UlValidateParms** est appelée différemment selon que le code appelant est C ou C++.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="c4ec8-127">Cette macro permet de valider les paramètres pour les méthodes **IUnknown** et MAPI qui renvoient ulong au lieu de valeurs HRESULT; la macro [ValidateParms](validateparms.md) fonctionne pour tous les autres.</span><span class="sxs-lookup"><span data-stu-id="c4ec8-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

