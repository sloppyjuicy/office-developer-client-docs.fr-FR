---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351323"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="6e72b-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="6e72b-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="6e72b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e72b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e72b-105">Indique l'emplacement dans un thread de message auquel un message appartient.</span><span class="sxs-lookup"><span data-stu-id="6e72b-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e72b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6e72b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6e72b-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="6e72b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6e72b-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="6e72b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6e72b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6e72b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6e72b-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="6e72b-110">Called by:</span></span>  <br/> |<span data-ttu-id="6e72b-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="6e72b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="6e72b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e72b-112">Parameters</span></span>

 <span data-ttu-id="6e72b-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="6e72b-113">_cbParent_</span></span>
  
> <span data-ttu-id="6e72b-114">dans Nombre d'octets dans l'index de conversation parente.</span><span class="sxs-lookup"><span data-stu-id="6e72b-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="6e72b-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="6e72b-115">_lpbParent_</span></span>
  
> <span data-ttu-id="6e72b-116">dans Pointeur vers des octets dans l'index de conversation parente.</span><span class="sxs-lookup"><span data-stu-id="6e72b-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="6e72b-117">Cette valeur peut être NULL si _cbParent_ est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6e72b-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="6e72b-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="6e72b-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="6e72b-119">remarquer Pointeur vers le nombre d'octets dans le nouvel index de conversation renvoyé par l'appel.</span><span class="sxs-lookup"><span data-stu-id="6e72b-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="6e72b-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="6e72b-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="6e72b-121">remarquer Pointeur vers un pointeur vers le nouvel index de conversation renvoyé par l'appel.</span><span class="sxs-lookup"><span data-stu-id="6e72b-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e72b-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6e72b-122">Return value</span></span>

<span data-ttu-id="6e72b-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e72b-123">S_OK</span></span> 
  
> <span data-ttu-id="6e72b-124">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6e72b-124">The call succeeded and has returned the expected value or values.</span></span>
    

