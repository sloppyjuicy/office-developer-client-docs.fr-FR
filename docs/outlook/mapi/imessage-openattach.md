---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405897"
---
# <a name="imessageopenattach"></a><span data-ttu-id="57ea2-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="57ea2-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="57ea2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57ea2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57ea2-105">Ouvre une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="57ea2-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="57ea2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57ea2-106">Parameters</span></span>

 <span data-ttu-id="57ea2-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="57ea2-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="57ea2-108">dans Numéro d'index de la pièce jointe à ouvrir, tel qu'il est stocké dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="57ea2-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="57ea2-109">Ce numéro d'index identifie de manière unique la pièce jointe dans le message et est valide uniquement dans le contexte du message.</span><span class="sxs-lookup"><span data-stu-id="57ea2-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="57ea2-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="57ea2-110">_lpInterface_</span></span>
  
> <span data-ttu-id="57ea2-111">dans Pointeur vers l'identificateur d'interface (IID) représentant l'interface à utiliser pour accéder à la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="57ea2-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="57ea2-112">Le fait de transmettre des résultats NULL dans l'interface standard de la pièce jointe, ou **IAttach**, est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="57ea2-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="57ea2-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57ea2-113">_ulFlags_</span></span>
  
> <span data-ttu-id="57ea2-114">dans Masque de des indicateurs qui contrôle la manière dont la pièce jointe est ouverte.</span><span class="sxs-lookup"><span data-stu-id="57ea2-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="57ea2-115">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="57ea2-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="57ea2-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="57ea2-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="57ea2-117">Demande l'ouverture de la pièce jointe avec les autorisations réseau maximales accordées à l'utilisateur et l'accès maximal de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="57ea2-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="57ea2-118">Par exemple, si le client dispose d'une autorisation en lecture/écriture, la pièce jointe doit être ouverte avec une autorisation en lecture/écriture; Si le client dispose d'un accès en lecture seule, la pièce jointe doit être ouverte avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="57ea2-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="57ea2-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="57ea2-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="57ea2-120">Permet à **OpenAttach** de renvoyer correctement, éventuellement avant que la pièce jointe soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="57ea2-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="57ea2-121">Si la pièce jointe n'est pas disponible, un appel ultérieur de celle-ci peut entraîner une erreur.</span><span class="sxs-lookup"><span data-stu-id="57ea2-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="57ea2-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="57ea2-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="57ea2-123">Demande une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="57ea2-123">Requests read/write permission.</span></span> <span data-ttu-id="57ea2-124">Par défaut, les pièces jointes sont ouvertes avec un accès en lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée.</span><span class="sxs-lookup"><span data-stu-id="57ea2-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="57ea2-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="57ea2-125">_lppAttach_</span></span>
  
> <span data-ttu-id="57ea2-126">remarquer Pointeur vers un pointeur vers la pièce jointe ouverte.</span><span class="sxs-lookup"><span data-stu-id="57ea2-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57ea2-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57ea2-127">Return value</span></span>

<span data-ttu-id="57ea2-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="57ea2-128">S_OK</span></span> 
  
> <span data-ttu-id="57ea2-129">La pièce jointe a été ouverte.</span><span class="sxs-lookup"><span data-stu-id="57ea2-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57ea2-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="57ea2-130">Remarks</span></span>

<span data-ttu-id="57ea2-131">La méthode **IMessage:: OpenAttach** ouvre la pièce jointe d'un message.</span><span class="sxs-lookup"><span data-stu-id="57ea2-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="57ea2-132">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="57ea2-132">Notes to callers</span></span>

<span data-ttu-id="57ea2-133">Pour ouvrir une pièce jointe, vous devez avoir accès à son numéro de pièce jointe ou à sa propriété **PR_ATTACH_NUM** .</span><span class="sxs-lookup"><span data-stu-id="57ea2-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="57ea2-134">Appelez [IMessage:: GetAttachmentTable](imessage-getattachmenttable.md) pour récupérer la table de pièces jointes du message et recherchez la ligne qui représente la pièce jointe à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="57ea2-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="57ea2-135">Pour plus d'informations, consultez la rubrique [ouverture d'une pièce jointe](opening-an-attachment.md) .</span><span class="sxs-lookup"><span data-stu-id="57ea2-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="57ea2-136">N'essayez pas d'ouvrir une pièce jointe plusieurs fois; les résultats ne sont pas définis et dépendants du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="57ea2-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="57ea2-137">Vous pouvez demander que la pièce jointe soit ouverte en mode lecture/écriture, au lieu du mode de lecture seule par défaut.</span><span class="sxs-lookup"><span data-stu-id="57ea2-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="57ea2-138">Toutefois, si la pièce jointe est ouverte en mode lecture/écriture, c'est au fournisseur de banque de messages de s'ouvrir.</span><span class="sxs-lookup"><span data-stu-id="57ea2-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="57ea2-139">Vous pouvez essayer de modifier la pièce jointe, de préparer la gestion d'un échec possible ou de vérifier le niveau d'accès accordé en récupérant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de la pièce jointe, si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="57ea2-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="57ea2-140">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="57ea2-140">MFCMAPI reference</span></span>

<span data-ttu-id="57ea2-141">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="57ea2-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="57ea2-142">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="57ea2-142">**File**</span></span>|<span data-ttu-id="57ea2-143">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="57ea2-143">**Function**</span></span>|<span data-ttu-id="57ea2-144">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="57ea2-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57ea2-145">AttachmentsDlg. cpp utilisé pour</span><span class="sxs-lookup"><span data-stu-id="57ea2-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="57ea2-146">CAttachmentsDlg:: OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="57ea2-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="57ea2-147">MFCMAPI utilise la méthode **IMessage:: OpenAttach** pour ouvrir les objets Attachment,</span><span class="sxs-lookup"><span data-stu-id="57ea2-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57ea2-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57ea2-148">See also</span></span>



[<span data-ttu-id="57ea2-149">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="57ea2-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="57ea2-150">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="57ea2-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

