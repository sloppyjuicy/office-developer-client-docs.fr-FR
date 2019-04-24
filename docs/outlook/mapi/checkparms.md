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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331800"
---
# <a name="checkparms"></a><span data-ttu-id="7aa9b-103">CheckParms</span><span class="sxs-lookup"><span data-stu-id="7aa9b-103">CheckParms</span></span>

  
  
<span data-ttu-id="7aa9b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7aa9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7aa9b-105">Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes du fournisseur de services appelées par MAPI.</span><span class="sxs-lookup"><span data-stu-id="7aa9b-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7aa9b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7aa9b-106">Header file:</span></span>  <br/> |<span data-ttu-id="7aa9b-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="7aa9b-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="7aa9b-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7aa9b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7aa9b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7aa9b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7aa9b-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7aa9b-110">Called by:</span></span>  <br/> |<span data-ttu-id="7aa9b-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7aa9b-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="7aa9b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7aa9b-112">Parameters</span></span>

 <span data-ttu-id="7aa9b-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="7aa9b-113">_eMethod_</span></span>
  
> <span data-ttu-id="7aa9b-114">dans Spécifie, par énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="7aa9b-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="7aa9b-115">_First_</span><span class="sxs-lookup"><span data-stu-id="7aa9b-115">_First_</span></span>
  
> <span data-ttu-id="7aa9b-116">dans Pointeur vers le premier argument de la pile.</span><span class="sxs-lookup"><span data-stu-id="7aa9b-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7aa9b-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7aa9b-117">Return value</span></span>

<span data-ttu-id="7aa9b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7aa9b-118">S_OK</span></span> 
  
> <span data-ttu-id="7aa9b-119">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="7aa9b-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7aa9b-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="7aa9b-120">Remarks</span></span>

<span data-ttu-id="7aa9b-121">Contrairement aux macros [ValidateParms](validateparms.md) et [UlValidateParms](ulvalidateparms.md) , la macro **CheckParms** n'effectue pas de validation de paramètre complète.</span><span class="sxs-lookup"><span data-stu-id="7aa9b-121">In contrast to the [ValidateParms](validateparms.md) and [UlValidateParms](ulvalidateparms.md) macros, the **CheckParms** macro does not perform a full parameter validation.</span></span> <span data-ttu-id="7aa9b-122">Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés corrects, de sorte que **CheckParms** effectue uniquement une validation de débogage.</span><span class="sxs-lookup"><span data-stu-id="7aa9b-122">Parameters passed between MAPI and service providers are assumed to be correct, so **CheckParms** performs a debug validation only.</span></span> 
  

