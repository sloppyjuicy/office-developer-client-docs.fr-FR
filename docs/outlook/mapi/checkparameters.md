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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a693c06d933c7e93d384aac8da8d5311eaf1d9da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783061"
---
# <a name="checkparameters"></a><span data-ttu-id="2fd7c-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="2fd7c-103">CheckParameters</span></span>

  
  
<span data-ttu-id="2fd7c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2fd7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2fd7c-105">Appelle une fonction interne pour valider les paramètres de débogage sur les méthodes de fournisseur de service appelées par MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fd7c-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2fd7c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2fd7c-106">Header file:</span></span>  <br/> |<span data-ttu-id="2fd7c-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2fd7c-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2fd7c-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="2fd7c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2fd7c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2fd7c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2fd7c-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="2fd7c-110">Called by:</span></span>  <br/> |<span data-ttu-id="2fd7c-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="2fd7c-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="2fd7c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fd7c-112">Parameters</span></span>

 <span data-ttu-id="2fd7c-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="2fd7c-113">_eMethod_</span></span>
  
> <span data-ttu-id="2fd7c-114">[in] Spécifie, par l’énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="2fd7c-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="2fd7c-115">_Premier_</span><span class="sxs-lookup"><span data-stu-id="2fd7c-115">_First_</span></span>
  
> <span data-ttu-id="2fd7c-116">[in] Pointeur vers le premier argument dans la pile.</span><span class="sxs-lookup"><span data-stu-id="2fd7c-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2fd7c-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2fd7c-117">Return value</span></span>

<span data-ttu-id="2fd7c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2fd7c-118">S_OK</span></span> 
  
> <span data-ttu-id="2fd7c-119">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="2fd7c-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2fd7c-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="2fd7c-120">Remarks</span></span>

<span data-ttu-id="2fd7c-121">La macro **CheckParameters** a été remplacée par la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd7c-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="2fd7c-122">**CheckParms** est recommandé sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="2fd7c-122">**CheckParms** is recommended on all platforms.</span></span> 
  

