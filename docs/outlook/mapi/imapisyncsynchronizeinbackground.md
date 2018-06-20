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
description: 'Dernière modification : 26 juin 2012'
ms.openlocfilehash: fd35d38cbb70431ab7fadbab3850a1585f9c6459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784065"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="be37c-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="be37c-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="be37c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be37c-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="be37c-105">Déclenche une synchronisation.</span><span class="sxs-lookup"><span data-stu-id="be37c-105">Initiates a synchronization.</span></span> <span data-ttu-id="be37c-106">Cette méthode est appelée par Microsoft Outlook 2010 et Microsoft Outlook 2013 et implémentée par les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="be37c-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="be37c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be37c-107">Parameters</span></span>

 <span data-ttu-id="be37c-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="be37c-108">_psibpb_</span></span>
  
> <span data-ttu-id="be37c-109">Informe le fournisseur de ce qui sera synchronisé et donne accès aux interfaces qui peuvent être utilisés lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="be37c-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="be37c-110">Il est une structure [MAPISIB](mapisib.md) .</span><span class="sxs-lookup"><span data-stu-id="be37c-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="be37c-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="be37c-111">Return value</span></span>

<span data-ttu-id="be37c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="be37c-112">S_OK</span></span> 
  
> <span data-ttu-id="be37c-113">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="be37c-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be37c-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be37c-114">See also</span></span>



[<span data-ttu-id="be37c-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be37c-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="be37c-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="be37c-116">MAPISIB</span></span>](mapisib.md)

