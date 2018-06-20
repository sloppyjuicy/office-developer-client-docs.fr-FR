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
ms.openlocfilehash: 12b1655b1e6786d2ebc985e834b635679e59f7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787412"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="4635f-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="4635f-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="4635f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4635f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4635f-105">Appelle une fonction interne pour vérifier que les applications clientes de paramètres transmis à MAPI et les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="4635f-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4635f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4635f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4635f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="4635f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="4635f-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="4635f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4635f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4635f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4635f-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="4635f-110">Called by:</span></span>  <br/> |<span data-ttu-id="4635f-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="4635f-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="4635f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4635f-112">Parameters</span></span>

 <span data-ttu-id="4635f-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="4635f-113">_eMethod_</span></span>
  
> <span data-ttu-id="4635f-114">[in] Spécifie, par l’énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="4635f-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="4635f-115">_Premier_</span><span class="sxs-lookup"><span data-stu-id="4635f-115">_First_</span></span>
  
> <span data-ttu-id="4635f-116">[in] Pointeur vers le premier argument dans la pile.</span><span class="sxs-lookup"><span data-stu-id="4635f-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4635f-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4635f-117">Return value</span></span>

<span data-ttu-id="4635f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4635f-118">S_OK</span></span> 
  
> <span data-ttu-id="4635f-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4635f-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4635f-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="4635f-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="4635f-121">Une erreur a empêché l’opération de se terminer.</span><span class="sxs-lookup"><span data-stu-id="4635f-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4635f-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="4635f-122">Remarks</span></span>

<span data-ttu-id="4635f-123">Paramètres passés entre MAPI et service fournisseurs sont supposés être correct et sont soumis à la validation de débogage uniquement avec la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="4635f-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="4635f-124">Fournisseurs doivent vérifier tous les paramètres passés par les applications clientes, mais les clients doivent supposer que MAPI et le fournisseur de paramètres sont corrects.</span><span class="sxs-lookup"><span data-stu-id="4635f-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="4635f-125">Utilisez la macro **HR_FAILED** pour tester les valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="4635f-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="4635f-126">La macro **UlValidateParms** est appelée différemment selon que le code appelant est C ou C++.</span><span class="sxs-lookup"><span data-stu-id="4635f-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="4635f-127">Cette macro est utilisée pour valider les paramètres pour les quelques méthodes **IUnknown** et MAPI qui renvoient ULONG au lieu des valeurs HRESULT ; la macro [ValidateParms](validateparms.md) fonctionne pour tous les autres.</span><span class="sxs-lookup"><span data-stu-id="4635f-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

