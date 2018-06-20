---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0f9aa5d508afeaf5933c50763e1e42832ae4e3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784118"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="6c0c2-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="6c0c2-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="6c0c2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c0c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c0c2-105">Avertit la visionneuse de formulaire le message actuel dans un formulaire a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="6c0c2-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="6c0c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c0c2-106">Parameters</span></span>

<span data-ttu-id="6c0c2-107">Aucune</span><span class="sxs-lookup"><span data-stu-id="6c0c2-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6c0c2-108">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6c0c2-108">Return value</span></span>

<span data-ttu-id="6c0c2-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c0c2-109">S_OK</span></span> 
  
> <span data-ttu-id="6c0c2-110">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6c0c2-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c0c2-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c0c2-111">Remarks</span></span>

<span data-ttu-id="6c0c2-112">Un objet form appelle la méthode **IMAPIViewAdviseSink::OnSaved** une fois que le message actuel dans un formulaire a été enregistré avec succès.</span><span class="sxs-lookup"><span data-stu-id="6c0c2-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="6c0c2-113">Cela permet de visionneuses pour mettre à jour leurs windows pour refléter les modifications apportées au message.</span><span class="sxs-lookup"><span data-stu-id="6c0c2-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="6c0c2-114">Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="6c0c2-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6c0c2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c0c2-115">See also</span></span>



[<span data-ttu-id="6c0c2-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c0c2-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

