---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 587b8bbb7ac25a7977d8962535f1909464ffc248
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571100"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="69eec-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="69eec-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="69eec-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69eec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69eec-105">Demande que le message en cours est en attente de remise.</span><span class="sxs-lookup"><span data-stu-id="69eec-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="69eec-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="69eec-106">Parameters</span></span>

 <span data-ttu-id="69eec-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69eec-107">_ulFlags_</span></span>
  
> <span data-ttu-id="69eec-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont un message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="69eec-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="69eec-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="69eec-109">The following flag can be set:</span></span>
    
<span data-ttu-id="69eec-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="69eec-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="69eec-111">MAPI doit envoyer le message même si elle ne peut pas être envoyé immédiatement.</span><span class="sxs-lookup"><span data-stu-id="69eec-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="69eec-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="69eec-112">Return value</span></span>

<span data-ttu-id="69eec-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="69eec-113">S_OK</span></span> 
  
> <span data-ttu-id="69eec-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="69eec-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69eec-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="69eec-115">Remarks</span></span>

<span data-ttu-id="69eec-116">Objets de formulaire appeler la méthode **IMAPIMessageSite::SubmitMessage** pour demander qu’un message est en attente de remise.</span><span class="sxs-lookup"><span data-stu-id="69eec-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="69eec-117">Le site de message doit appeler la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) avant d’envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="69eec-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="69eec-118">Le message n’a pas besoin avoir été précédemment enregistré, car **SubmitMessage** doit provoquer le message d’être enregistré si le message a été modifié.</span><span class="sxs-lookup"><span data-stu-id="69eec-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="69eec-119">Après le retour de **SubmitMessage**, le formulaire doit rechercher un message en cours et puis faire disparaître si aucune n’existe.</span><span class="sxs-lookup"><span data-stu-id="69eec-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="69eec-120">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="69eec-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="69eec-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="69eec-121">MFCMAPI reference</span></span>

<span data-ttu-id="69eec-122">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69eec-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="69eec-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="69eec-123">**File**</span></span>|<span data-ttu-id="69eec-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="69eec-124">**Function**</span></span>|<span data-ttu-id="69eec-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="69eec-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69eec-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="69eec-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="69eec-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="69eec-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="69eec-128">MFCMAPI utilise la méthode **IMAPIMessageSite::SubmitMessage** pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="69eec-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="69eec-129">Tout d’abord, il appelle la méthode **IPersistMessage::HandsOffMessage** , et il appelle ensuite **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="69eec-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69eec-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69eec-130">See also</span></span>



[<span data-ttu-id="69eec-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="69eec-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="69eec-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69eec-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="69eec-133">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="69eec-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="69eec-134">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="69eec-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

