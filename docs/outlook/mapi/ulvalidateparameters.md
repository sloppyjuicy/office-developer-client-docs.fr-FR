---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431273"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="36411-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="36411-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="36411-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36411-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36411-105">Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmises aux fournisseurs de services et MAPI.</span><span class="sxs-lookup"><span data-stu-id="36411-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36411-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="36411-106">Header file:</span></span>  <br/> |<span data-ttu-id="36411-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="36411-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="36411-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="36411-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="36411-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36411-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36411-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="36411-110">Called by:</span></span>  <br/> |<span data-ttu-id="36411-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="36411-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="36411-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36411-112">Parameters</span></span>

 <span data-ttu-id="36411-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="36411-113">_eMethod_</span></span>
  
> <span data-ttu-id="36411-114">dans Spécifie, par énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="36411-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="36411-115">_First_</span><span class="sxs-lookup"><span data-stu-id="36411-115">_First_</span></span>
  
> <span data-ttu-id="36411-116">dans Pointeur vers le premier argument de la pile.</span><span class="sxs-lookup"><span data-stu-id="36411-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36411-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="36411-117">Return value</span></span>

<span data-ttu-id="36411-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="36411-118">S_OK</span></span> 
  
> <span data-ttu-id="36411-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="36411-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="36411-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="36411-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="36411-121">Une erreur d'origine inattendue ou inconnue a empêché l'opération de s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="36411-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36411-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="36411-122">Remarks</span></span>

<span data-ttu-id="36411-123">La macro **UlValidateParameters** a été remplacée par la macro [UlValidateParms](ulvalidateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="36411-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="36411-124">**UlValidateParameters** ne fonctionne pas correctement sur les plateformes RISC et ne peut plus être compilé sur ces plateformes.</span><span class="sxs-lookup"><span data-stu-id="36411-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="36411-125">Il se compile et fonctionne correctement sur les plateformes Intel, mais **UlValidateParms** est recommandé sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="36411-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

