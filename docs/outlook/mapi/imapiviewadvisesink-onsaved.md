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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407605"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="f000b-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="f000b-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="f000b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f000b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f000b-105">Avertit la visionneuse de formulaire que le message en cours dans un formulaire a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="f000b-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="f000b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f000b-106">Parameters</span></span>

<span data-ttu-id="f000b-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="f000b-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f000b-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f000b-108">Return value</span></span>

<span data-ttu-id="f000b-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="f000b-109">S_OK</span></span> 
  
> <span data-ttu-id="f000b-110">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f000b-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f000b-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="f000b-111">Remarks</span></span>

<span data-ttu-id="f000b-112">Un objet de formulaire appelle la méthode **IMAPIViewAdviseSink::OnSaved** une fois que le message en cours dans un formulaire a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="f000b-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="f000b-113">Cela permet aux visiteurs de mettre à jour leurs fenêtres pour refléter les modifications apportées au message.</span><span class="sxs-lookup"><span data-stu-id="f000b-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="f000b-114">Pour plus d’informations sur les notifications de formulaire, voir [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f000b-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f000b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f000b-115">See also</span></span>



[<span data-ttu-id="f000b-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f000b-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

