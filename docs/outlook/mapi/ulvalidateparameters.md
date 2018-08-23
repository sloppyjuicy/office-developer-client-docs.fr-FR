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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 297b5a516f8275b236092f9f385afcb673c95de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585240"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="6fd8c-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="6fd8c-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="6fd8c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fd8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fd8c-105">Appelle une fonction interne pour vérifier que les applications clientes de paramètres transmis à MAPI et les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="6fd8c-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6fd8c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6fd8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="6fd8c-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="6fd8c-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="6fd8c-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6fd8c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6fd8c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6fd8c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6fd8c-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6fd8c-110">Called by:</span></span>  <br/> |<span data-ttu-id="6fd8c-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="6fd8c-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="6fd8c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fd8c-112">Parameters</span></span>

 <span data-ttu-id="6fd8c-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="6fd8c-113">_eMethod_</span></span>
  
> <span data-ttu-id="6fd8c-114">[in] Spécifie, par l’énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="6fd8c-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="6fd8c-115">_Premier_</span><span class="sxs-lookup"><span data-stu-id="6fd8c-115">_First_</span></span>
  
> <span data-ttu-id="6fd8c-116">[in] Pointeur vers le premier argument dans la pile.</span><span class="sxs-lookup"><span data-stu-id="6fd8c-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fd8c-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6fd8c-117">Return value</span></span>

<span data-ttu-id="6fd8c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fd8c-118">S_OK</span></span> 
  
> <span data-ttu-id="6fd8c-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6fd8c-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="6fd8c-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="6fd8c-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="6fd8c-121">Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.</span><span class="sxs-lookup"><span data-stu-id="6fd8c-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fd8c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="6fd8c-122">Remarks</span></span>

<span data-ttu-id="6fd8c-123">La macro **UlValidateParameters** a été remplacée par la macro [UlValidateParms](ulvalidateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="6fd8c-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="6fd8c-124">**UlValidateParameters** ne fonctionne pas correctement sur les plateformes RISC et est maintenant interdit la compilation sur les.</span><span class="sxs-lookup"><span data-stu-id="6fd8c-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="6fd8c-125">Il compile et fonctionne correctement sur les plateformes Intel, mais **UlValidateParms** est recommandé sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="6fd8c-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

