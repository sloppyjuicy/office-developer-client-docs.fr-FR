---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a922b8bb21bfd534935d4d1706a6ccfd15c2da5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433394"
---
# <a name="checkparameters"></a><span data-ttu-id="40b32-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="40b32-103">CheckParameters</span></span>

  
  
<span data-ttu-id="40b32-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40b32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40b32-105">Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de services appelées par MAPI.</span><span class="sxs-lookup"><span data-stu-id="40b32-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40b32-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="40b32-106">Header file:</span></span>  <br/> |<span data-ttu-id="40b32-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="40b32-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="40b32-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="40b32-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="40b32-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="40b32-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="40b32-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="40b32-110">Called by:</span></span>  <br/> |<span data-ttu-id="40b32-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="40b32-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="40b32-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40b32-112">Parameters</span></span>

 <span data-ttu-id="40b32-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="40b32-113">_eMethod_</span></span>
  
> <span data-ttu-id="40b32-114">[in] Spécifie, par l’éumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="40b32-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="40b32-115">_First_</span><span class="sxs-lookup"><span data-stu-id="40b32-115">_First_</span></span>
  
> <span data-ttu-id="40b32-116">[in] Pointeur vers le premier argument de la pile.</span><span class="sxs-lookup"><span data-stu-id="40b32-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40b32-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="40b32-117">Return value</span></span>

<span data-ttu-id="40b32-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="40b32-118">S_OK</span></span> 
  
> <span data-ttu-id="40b32-119">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="40b32-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40b32-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="40b32-120">Remarks</span></span>

<span data-ttu-id="40b32-121">La macro **CheckParameters** a été recalée par la macro [CheckParms.](checkparms.md)</span><span class="sxs-lookup"><span data-stu-id="40b32-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="40b32-122">**CheckParms est** recommandé sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="40b32-122">**CheckParms** is recommended on all platforms.</span></span> 
  

