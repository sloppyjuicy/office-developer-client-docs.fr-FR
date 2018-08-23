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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3612c12a503174484d4a469ffa167922a015ed5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576609"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="d0b19-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="d0b19-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="d0b19-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0b19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0b19-105">Renvoie le message en cours.</span><span class="sxs-lookup"><span data-stu-id="d0b19-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="d0b19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0b19-106">Parameters</span></span>

 <span data-ttu-id="d0b19-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="d0b19-107">_ppmsg_</span></span>
  
> <span data-ttu-id="d0b19-108">[out] Pointeur vers un pointeur vers l’interface retournée pour le message.</span><span class="sxs-lookup"><span data-stu-id="d0b19-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0b19-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d0b19-109">Return value</span></span>

<span data-ttu-id="d0b19-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0b19-110">S_OK</span></span> 
  
> <span data-ttu-id="d0b19-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d0b19-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d0b19-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d0b19-112">S_FALSE</span></span> 
  
> <span data-ttu-id="d0b19-113">Aucun message n’existe actuellement pour le formulaire d’appel.</span><span class="sxs-lookup"><span data-stu-id="d0b19-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0b19-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0b19-114">Remarks</span></span>

<span data-ttu-id="d0b19-115">Formulaires appeler la méthode **IMAPIMessageSite::GetMessage** pour obtenir une interface de message pour le message en cours.</span><span class="sxs-lookup"><span data-stu-id="d0b19-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="d0b19-116">Le message en cours est le même message, comme la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)ou [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) a été passé précédemment.</span><span class="sxs-lookup"><span data-stu-id="d0b19-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="d0b19-117">**GetMessage** renvoie S_FALSE si aucun message n’existe actuellement.</span><span class="sxs-lookup"><span data-stu-id="d0b19-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="d0b19-118">Cet état peut se produire après des appels à la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) ou avant l’appel suivant à **IPersistMessage::Load** ou **IPersistMessage::SaveCompleted** est établie.</span><span class="sxs-lookup"><span data-stu-id="d0b19-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="d0b19-119">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d0b19-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d0b19-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d0b19-120">MFCMAPI reference</span></span>

<span data-ttu-id="d0b19-121">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d0b19-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d0b19-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="d0b19-122">**File**</span></span>|<span data-ttu-id="d0b19-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="d0b19-123">**Function**</span></span>|<span data-ttu-id="d0b19-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="d0b19-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0b19-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d0b19-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d0b19-126">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="d0b19-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="d0b19-127">MFCMAPI utilise la méthode **IMAPIMessageSite::GetMessage** pour renvoyer le pointeur de message actuellement mis en cache, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="d0b19-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0b19-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0b19-128">See also</span></span>



[<span data-ttu-id="d0b19-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="d0b19-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="d0b19-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="d0b19-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="d0b19-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0b19-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="d0b19-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="d0b19-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="d0b19-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="d0b19-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="d0b19-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0b19-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d0b19-135">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="d0b19-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d0b19-136">Interfaces de formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="d0b19-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

