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
ms.openlocfilehash: 43765cddb2f06bfbe58e0a4000c7eadfdc5f3347
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787077"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="0f36e-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="0f36e-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="0f36e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f36e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f36e-105">Indique où dans un thread de message, un message appartient.</span><span class="sxs-lookup"><span data-stu-id="0f36e-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f36e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0f36e-106">Header file:</span></span>  <br/> |<span data-ttu-id="0f36e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0f36e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0f36e-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="0f36e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0f36e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0f36e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0f36e-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="0f36e-110">Called by:</span></span>  <br/> |<span data-ttu-id="0f36e-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="0f36e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="0f36e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f36e-112">Parameters</span></span>

 <span data-ttu-id="0f36e-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="0f36e-113">_cbParent_</span></span>
  
> <span data-ttu-id="0f36e-114">[in] Nombre d’octets dans l’index de conversation parent.</span><span class="sxs-lookup"><span data-stu-id="0f36e-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="0f36e-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="0f36e-115">_lpbParent_</span></span>
  
> <span data-ttu-id="0f36e-116">[in] Pointeur vers les octets dans l’index de conversation parent.</span><span class="sxs-lookup"><span data-stu-id="0f36e-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="0f36e-117">Cela peut être NULL si _cbParent_ est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="0f36e-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="0f36e-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="0f36e-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="0f36e-119">[out] Pointeur vers le nombre d’octets dans le nouvel index de conversation renvoyé par l’appel.</span><span class="sxs-lookup"><span data-stu-id="0f36e-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="0f36e-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="0f36e-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="0f36e-121">[out] Pointeur vers un pointeur vers le nouvel index de conversation renvoyé par l’appel.</span><span class="sxs-lookup"><span data-stu-id="0f36e-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f36e-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="0f36e-122">Return value</span></span>

<span data-ttu-id="0f36e-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f36e-123">S_OK</span></span> 
  
> <span data-ttu-id="0f36e-124">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="0f36e-124">The call succeeded and has returned the expected value or values.</span></span>
    

