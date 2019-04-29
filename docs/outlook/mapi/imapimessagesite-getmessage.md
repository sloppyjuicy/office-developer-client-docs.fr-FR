---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409026"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="69f22-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="69f22-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="69f22-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69f22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69f22-105">Renvoie le message actif.</span><span class="sxs-lookup"><span data-stu-id="69f22-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="69f22-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69f22-106">Parameters</span></span>

 <span data-ttu-id="69f22-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="69f22-107">_ppmsg_</span></span>
  
> <span data-ttu-id="69f22-108">remarquer Pointeur vers un pointeur vers l'interface renvoyée pour le message.</span><span class="sxs-lookup"><span data-stu-id="69f22-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="69f22-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="69f22-109">Return value</span></span>

<span data-ttu-id="69f22-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="69f22-110">S_OK</span></span> 
  
> <span data-ttu-id="69f22-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="69f22-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="69f22-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="69f22-112">S_FALSE</span></span> 
  
> <span data-ttu-id="69f22-113">Il n'existe actuellement aucun message pour le formulaire appelant.</span><span class="sxs-lookup"><span data-stu-id="69f22-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69f22-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="69f22-114">Remarks</span></span>

<span data-ttu-id="69f22-115">Les formulaires appellent la méthode **IMAPIMessageSite:: GetMessage** pour obtenir une interface de message pour le message en cours.</span><span class="sxs-lookup"><span data-stu-id="69f22-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="69f22-116">Le message actif est le même message que celui précédemment transmis dans la méthode [IPersistMessage:: InitNew](ipersistmessage-initnew.md), [IPersistMessage:: Load](ipersistmessage-load.md), ou [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="69f22-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="69f22-117">**GetMessage** renvoie S_FALSE si aucun message n'existe actuellement.</span><span class="sxs-lookup"><span data-stu-id="69f22-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="69f22-118">Cet État peut se produire après les appels à la méthode [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) ou avant l'appel suivant à **IPersistMessage:: Load** ou **IPersistMessage:: SaveCompleted** est effectué.</span><span class="sxs-lookup"><span data-stu-id="69f22-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="69f22-119">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="69f22-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="69f22-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="69f22-120">MFCMAPI reference</span></span>

<span data-ttu-id="69f22-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69f22-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="69f22-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="69f22-122">**File**</span></span>|<span data-ttu-id="69f22-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="69f22-123">**Function**</span></span>|<span data-ttu-id="69f22-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="69f22-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69f22-125">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="69f22-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="69f22-126">CMyMAPIFormViewer:: GetSession</span><span class="sxs-lookup"><span data-stu-id="69f22-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="69f22-127">MFCMAPI utilise la méthode **IMAPIMessageSite:: GetMessage** pour renvoyer le pointeur de message actuellement mis en cache, s'il est disponible.</span><span class="sxs-lookup"><span data-stu-id="69f22-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69f22-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69f22-128">See also</span></span>



[<span data-ttu-id="69f22-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="69f22-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="69f22-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="69f22-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="69f22-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69f22-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="69f22-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="69f22-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="69f22-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="69f22-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="69f22-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69f22-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="69f22-135">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="69f22-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="69f22-136">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="69f22-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

