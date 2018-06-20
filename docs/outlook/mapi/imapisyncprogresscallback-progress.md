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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 12624ef6212f9113041bf5cf3a82e2b7df6eca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784051"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="7b8de-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="7b8de-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="7b8de-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b8de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b8de-105">Met à jour l’état dans la boîte de dialogue d’envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="7b8de-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="7b8de-106">Le fournisseur de banque appelle régulièrement cette fonction.</span><span class="sxs-lookup"><span data-stu-id="7b8de-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="7b8de-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b8de-107">Parameters</span></span>

 <span data-ttu-id="7b8de-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="7b8de-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="7b8de-109">Pointeur vers une chaîne qui affiche l’étape de progression en cours.</span><span class="sxs-lookup"><span data-stu-id="7b8de-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="7b8de-110">Il peut être NULL pour mettre à jour l’avancement.</span><span class="sxs-lookup"><span data-stu-id="7b8de-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="7b8de-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="7b8de-111">**ulIndex**</span></span>
  
> <span data-ttu-id="7b8de-112">La position actuelle en cours.</span><span class="sxs-lookup"><span data-stu-id="7b8de-112">The current position in progress.</span></span>
    
 <span data-ttu-id="7b8de-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="7b8de-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="7b8de-114">L’index indiquant la progression complète.</span><span class="sxs-lookup"><span data-stu-id="7b8de-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b8de-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7b8de-115">Return value</span></span>

<span data-ttu-id="7b8de-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b8de-116">S_OK</span></span> 
  
> <span data-ttu-id="7b8de-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="7b8de-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b8de-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b8de-118">See also</span></span>



[<span data-ttu-id="7b8de-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b8de-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

