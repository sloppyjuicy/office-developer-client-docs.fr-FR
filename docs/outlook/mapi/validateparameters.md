---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425202"
---
# <a name="validateparameters"></a><span data-ttu-id="30afc-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="30afc-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="30afc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30afc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30afc-105">Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmises aux fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="30afc-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30afc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="30afc-106">Header file:</span></span>  <br/> |<span data-ttu-id="30afc-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="30afc-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="30afc-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="30afc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="30afc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="30afc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="30afc-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="30afc-110">Called by:</span></span>  <br/> |<span data-ttu-id="30afc-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="30afc-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="30afc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30afc-112">Parameters</span></span>

 <span data-ttu-id="30afc-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="30afc-113">_eMethod_</span></span>
  
> <span data-ttu-id="30afc-114">dans Spécifie, par énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="30afc-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="30afc-115">_First_</span><span class="sxs-lookup"><span data-stu-id="30afc-115">_First_</span></span>
  
> <span data-ttu-id="30afc-116">dans Pointeur vers le premier argument de la pile.</span><span class="sxs-lookup"><span data-stu-id="30afc-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="30afc-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="30afc-117">Return value</span></span>

<span data-ttu-id="30afc-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="30afc-118">S_OK</span></span> 
  
> <span data-ttu-id="30afc-119">Tous les paramètres sont valides.</span><span class="sxs-lookup"><span data-stu-id="30afc-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="30afc-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="30afc-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="30afc-121">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="30afc-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30afc-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="30afc-122">Remarks</span></span>

<span data-ttu-id="30afc-123">La macro **ValidateParameters** a été remplacée par la macro [ValidateParms](validateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="30afc-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="30afc-124">**ValidateParameters** ne fonctionne pas correctement sur les plateformes RISC et ne peut plus être compilé sur ces plateformes.</span><span class="sxs-lookup"><span data-stu-id="30afc-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="30afc-125">Il se compile et fonctionne correctement sur les plateformes Intel, mais **ValidateParms** est recommandé sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="30afc-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

