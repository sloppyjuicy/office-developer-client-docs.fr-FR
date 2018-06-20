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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 921417d8fc73ca9c1f126b2cb0add23f6625e3f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787462"
---
# <a name="validateparameters"></a><span data-ttu-id="8715f-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="8715f-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="8715f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8715f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8715f-105">Appelle une fonction interne pour vérifier que les applications clientes de paramètres transmis à des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="8715f-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8715f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8715f-106">Header file:</span></span>  <br/> |<span data-ttu-id="8715f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="8715f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="8715f-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="8715f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8715f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8715f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8715f-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="8715f-110">Called by:</span></span>  <br/> |<span data-ttu-id="8715f-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="8715f-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="8715f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8715f-112">Parameters</span></span>

 <span data-ttu-id="8715f-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="8715f-113">_eMethod_</span></span>
  
> <span data-ttu-id="8715f-114">[in] Spécifie, par l’énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="8715f-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="8715f-115">_Premier_</span><span class="sxs-lookup"><span data-stu-id="8715f-115">_First_</span></span>
  
> <span data-ttu-id="8715f-116">[in] Pointeur vers le premier argument dans la pile.</span><span class="sxs-lookup"><span data-stu-id="8715f-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8715f-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8715f-117">Return value</span></span>

<span data-ttu-id="8715f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8715f-118">S_OK</span></span> 
  
> <span data-ttu-id="8715f-119">Tous les paramètres sont valides.</span><span class="sxs-lookup"><span data-stu-id="8715f-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="8715f-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="8715f-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="8715f-121">Un ou plusieurs des paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="8715f-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8715f-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="8715f-122">Remarks</span></span>

<span data-ttu-id="8715f-123">La macro **ValidateParameters** a été remplacée par la macro [ValidateParms](validateparms.md) .</span><span class="sxs-lookup"><span data-stu-id="8715f-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="8715f-124">**ValidateParameters** ne fonctionne pas correctement sur les plateformes RISC et est maintenant interdit la compilation sur les.</span><span class="sxs-lookup"><span data-stu-id="8715f-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="8715f-125">Il compile et fonctionne correctement sur les plateformes Intel, mais **ValidateParms** est recommandé sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="8715f-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

