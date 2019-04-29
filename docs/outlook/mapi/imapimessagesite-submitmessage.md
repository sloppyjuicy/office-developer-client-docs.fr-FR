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
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417027"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="e1fef-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e1fef-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="e1fef-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1fef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1fef-105">Demande que le message en cours soit mis en file d'attente pour remise.</span><span class="sxs-lookup"><span data-stu-id="e1fef-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e1fef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1fef-106">Parameters</span></span>

 <span data-ttu-id="e1fef-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1fef-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e1fef-108">dans Masque de des indicateurs qui contrôle le mode d'envoi d'un message.</span><span class="sxs-lookup"><span data-stu-id="e1fef-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="e1fef-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="e1fef-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e1fef-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="e1fef-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="e1fef-111">MAPI doit envoyer le message même s'il ne peut pas être envoyé immédiatement.</span><span class="sxs-lookup"><span data-stu-id="e1fef-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1fef-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e1fef-112">Return value</span></span>

<span data-ttu-id="e1fef-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1fef-113">S_OK</span></span> 
  
> <span data-ttu-id="e1fef-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e1fef-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1fef-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1fef-115">Remarks</span></span>

<span data-ttu-id="e1fef-116">Les objets de formulaire appellent la méthode **IMAPIMessageSite:: SubmitMessage** pour demander qu'un message soit mis en file d'attente pour remise.</span><span class="sxs-lookup"><span data-stu-id="e1fef-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="e1fef-117">Le site de message doit appeler la méthode [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) avant d'envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="e1fef-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="e1fef-118">Le message n'a pas besoin d'avoir été précédemment enregistré, car **SubmitMessage** doit entraîner l'enregistrement du message si celui-ci a été modifié.</span><span class="sxs-lookup"><span data-stu-id="e1fef-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="e1fef-119">Après le retour de **SubmitMessage**, le formulaire doit vérifier l'existence d'un message en cours, puis le faire disparaître s'il n'en existe pas.</span><span class="sxs-lookup"><span data-stu-id="e1fef-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="e1fef-120">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="e1fef-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e1fef-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e1fef-121">MFCMAPI reference</span></span>

<span data-ttu-id="e1fef-122">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e1fef-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e1fef-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e1fef-123">**File**</span></span>|<span data-ttu-id="e1fef-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e1fef-124">**Function**</span></span>|<span data-ttu-id="e1fef-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e1fef-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1fef-126">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="e1fef-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="e1fef-127">CMyMAPIFormViewer:: SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e1fef-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="e1fef-128">MFCMAPI utilise la méthode **IMAPIMessageSite:: SubmitMessage** pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="e1fef-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="e1fef-129">Tout d'abord, il appelle la méthode **IPersistMessage:: HandsOffMessage** , puis appelle **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="e1fef-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1fef-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1fef-130">See also</span></span>



[<span data-ttu-id="e1fef-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="e1fef-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="e1fef-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1fef-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="e1fef-133">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e1fef-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e1fef-134">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="e1fef-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

