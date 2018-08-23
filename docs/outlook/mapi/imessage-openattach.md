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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 48df5362106e849f061b0797736fad82fafa6584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588712"
---
# <a name="imessageopenattach"></a><span data-ttu-id="ce44c-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="ce44c-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="ce44c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce44c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce44c-105">Ouvre une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ce44c-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="ce44c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce44c-106">Parameters</span></span>

 <span data-ttu-id="ce44c-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="ce44c-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="ce44c-108">[in] Numéro d’index de la pièce jointe à ouvrir, tel que stocké dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ce44c-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="ce44c-109">Ce numéro d’index identifie la pièce jointe dans le message unique et est valide uniquement dans le contexte du message.</span><span class="sxs-lookup"><span data-stu-id="ce44c-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="ce44c-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ce44c-110">_lpInterface_</span></span>
  
> <span data-ttu-id="ce44c-111">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ce44c-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="ce44c-112">Transmission NULL génère interface standard de la pièce jointe, ou **IAttach**, renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ce44c-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="ce44c-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce44c-113">_ulFlags_</span></span>
  
> <span data-ttu-id="ce44c-114">[in] Masque de bits d’indicateurs qui contrôle la façon dont la pièce jointe est ouverte.</span><span class="sxs-lookup"><span data-stu-id="ce44c-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="ce44c-115">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="ce44c-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="ce44c-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ce44c-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="ce44c-117">Demande que la pièce jointe s’ouvre avec les autorisations de réseau maximale autorisées pour l’accès des utilisateurs et le nombre maximal de clients application.</span><span class="sxs-lookup"><span data-stu-id="ce44c-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="ce44c-118">Par exemple, si le client a l’autorisation de lecture/écriture, la pièce jointe doit être ouvert avec l’autorisation de lecture/écriture ; Si le client dispose d’un accès en lecture seule, la pièce jointe doit être ouvert avec accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ce44c-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="ce44c-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ce44c-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ce44c-120">Permet **OpenAttach** renvoyer avec succès, éventuellement avant la pièce jointe est totalement disponible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="ce44c-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="ce44c-121">Si la pièce jointe n’est pas disponible, vous appelez suivante lui peut provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="ce44c-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="ce44c-122">N'</span><span class="sxs-lookup"><span data-stu-id="ce44c-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ce44c-123">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ce44c-123">Requests read/write permission.</span></span> <span data-ttu-id="ce44c-124">Par défaut, les pièces jointes sont ouverts avec accès en lecture seule, et les clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ce44c-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="ce44c-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="ce44c-125">_lppAttach_</span></span>
  
> <span data-ttu-id="ce44c-126">[out] Pointeur vers un pointeur vers la pièce jointe ouverte.</span><span class="sxs-lookup"><span data-stu-id="ce44c-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce44c-127">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ce44c-127">Return value</span></span>

<span data-ttu-id="ce44c-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce44c-128">S_OK</span></span> 
  
> <span data-ttu-id="ce44c-129">La pièce jointe a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="ce44c-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce44c-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="ce44c-130">Remarks</span></span>

<span data-ttu-id="ce44c-131">La méthode **IMessage::OpenAttach** ouvre la pièce jointe d’un message.</span><span class="sxs-lookup"><span data-stu-id="ce44c-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ce44c-132">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="ce44c-132">Notes to callers</span></span>

<span data-ttu-id="ce44c-133">Pour ouvrir une pièce jointe, vous devez avoir accès à son nombre de pièces jointes ou d’une propriété **PR_ATTACH_NUM** .</span><span class="sxs-lookup"><span data-stu-id="ce44c-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="ce44c-134">Appelez [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) pour récupérer la table des pièces jointes du message et la ligne qui représente la pièce jointe à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="ce44c-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="ce44c-135">Pour plus d’informations, consultez [ouverture d’une pièce jointe](opening-an-attachment.md) .</span><span class="sxs-lookup"><span data-stu-id="ce44c-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="ce44c-136">N’essayez pas d’ouvrir une pièce jointe à plusieurs reprises ; les résultats sont undefined et varie selon le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="ce44c-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="ce44c-137">Vous pouvez demander que la pièce jointe s’ouvre en mode lecture/écriture, au lieu du mode par défaut en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ce44c-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="ce44c-138">Toutefois, si la pièce jointe sera réellement ouvert en mode lecture/écriture est le fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="ce44c-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="ce44c-139">Vous pouvez modifier la pièce jointe, essayez préparation gérer la défaillance ou vérifier le niveau d’accès qui a été accordé en récupérant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) de la pièce jointe, si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="ce44c-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ce44c-140">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ce44c-140">MFCMAPI reference</span></span>

<span data-ttu-id="ce44c-141">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ce44c-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ce44c-142">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ce44c-142">**File**</span></span>|<span data-ttu-id="ce44c-143">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ce44c-143">**Function**</span></span>|<span data-ttu-id="ce44c-144">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ce44c-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce44c-145">AttachmentsDlg.cpp utilisé pour</span><span class="sxs-lookup"><span data-stu-id="ce44c-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="ce44c-146">CAttachmentsDlg::OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="ce44c-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="ce44c-147">MFCMAPI utilise la méthode **IMessage::OpenAttach** pour ouvrir les objets attachment,</span><span class="sxs-lookup"><span data-stu-id="ce44c-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce44c-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce44c-148">See also</span></span>



[<span data-ttu-id="ce44c-149">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ce44c-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="ce44c-150">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ce44c-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

