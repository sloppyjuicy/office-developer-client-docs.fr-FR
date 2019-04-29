---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429109"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="37d66-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="37d66-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="37d66-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37d66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37d66-105">Met à jour l'État dans la boîte de dialogue d'envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="37d66-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="37d66-106">Le fournisseur de Banque appelle régulièrement cette fonction.</span><span class="sxs-lookup"><span data-stu-id="37d66-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="37d66-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37d66-107">Parameters</span></span>

 <span data-ttu-id="37d66-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="37d66-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="37d66-109">Pointeur vers une chaîne qui affiche l'étape de progression actuelle.</span><span class="sxs-lookup"><span data-stu-id="37d66-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="37d66-110">La valeur peut être NULL pour mettre à jour la progression.</span><span class="sxs-lookup"><span data-stu-id="37d66-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="37d66-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="37d66-111">**ulIndex**</span></span>
  
> <span data-ttu-id="37d66-112">Position actuelle en cours.</span><span class="sxs-lookup"><span data-stu-id="37d66-112">The current position in progress.</span></span>
    
 <span data-ttu-id="37d66-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="37d66-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="37d66-114">Index indiquant la progression complète.</span><span class="sxs-lookup"><span data-stu-id="37d66-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37d66-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="37d66-115">Return value</span></span>

<span data-ttu-id="37d66-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="37d66-116">S_OK</span></span> 
  
> <span data-ttu-id="37d66-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="37d66-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37d66-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37d66-118">See also</span></span>



[<span data-ttu-id="37d66-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37d66-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

