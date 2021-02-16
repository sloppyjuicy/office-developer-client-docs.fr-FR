---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Dernière modification : 26 juin 2012'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426855"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="a4c89-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="a4c89-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="a4c89-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4c89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a4c89-105">Lance une synchronisation.</span><span class="sxs-lookup"><span data-stu-id="a4c89-105">Initiates a synchronization.</span></span> <span data-ttu-id="a4c89-106">Cette méthode est appelée par Microsoft Outlook 2010 et Microsoft Outlook 2013 et implémentée par les fournisseurs de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="a4c89-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="a4c89-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4c89-107">Parameters</span></span>

 <span data-ttu-id="a4c89-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="a4c89-108">_psibpb_</span></span>
  
> <span data-ttu-id="a4c89-109">Informe le fournisseur de ce qui sera synchronisé et donne accès aux interfaces qui peuvent être utilisées pendant la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="a4c89-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="a4c89-110">Il s’agit [d’une structure MAPISIB.](mapisib.md)</span><span class="sxs-lookup"><span data-stu-id="a4c89-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a4c89-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a4c89-111">Return value</span></span>

<span data-ttu-id="a4c89-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4c89-112">S_OK</span></span> 
  
> <span data-ttu-id="a4c89-113">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a4c89-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4c89-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4c89-114">See also</span></span>



[<span data-ttu-id="a4c89-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4c89-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="a4c89-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="a4c89-116">MAPISIB</span></span>](mapisib.md)

