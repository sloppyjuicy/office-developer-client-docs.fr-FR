---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: de5c98272c08c469acf23b0ecae7eac0a2d1bfe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592513"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="879c2-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="879c2-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="879c2-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="879c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="879c2-105">Supprime une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="879c2-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="879c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="879c2-106">Parameters</span></span>

 <span data-ttu-id="879c2-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="879c2-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="879c2-108">[in] Numéro d’index de la pièce jointe à supprimer.</span><span class="sxs-lookup"><span data-stu-id="879c2-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="879c2-109">Il s’agit de la valeur de propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="879c2-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="879c2-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="879c2-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="879c2-111">[in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou de windows, que cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="879c2-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="879c2-112">Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur ATTACH_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="879c2-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="879c2-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="879c2-113">_lpProgress_</span></span>
  
> <span data-ttu-id="879c2-114">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="879c2-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="879c2-115">Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="879c2-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="879c2-116">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur ATTACH_DIALOG est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="879c2-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="879c2-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="879c2-117">_ulFlags_</span></span>
  
> <span data-ttu-id="879c2-118">[in] Masque de bits d’indicateurs qui contrôle l’affichage de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="879c2-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="879c2-119">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="879c2-119">The following flag can be set:</span></span>
    
<span data-ttu-id="879c2-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="879c2-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="879c2-121">Demande l’affichage d’un indicateur de progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="879c2-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="879c2-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="879c2-122">Return value</span></span>

<span data-ttu-id="879c2-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="879c2-123">S_OK</span></span> 
  
> <span data-ttu-id="879c2-124">La pièce jointe a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="879c2-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="879c2-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="879c2-125">Remarks</span></span>

<span data-ttu-id="879c2-126">La méthode **IMessage::DeleteAttach** supprime une pièce jointe à partir d’un message.</span><span class="sxs-lookup"><span data-stu-id="879c2-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="879c2-127">Une pièce jointe supprimée n’est pas définitivement supprimée jusqu'à ce que la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message a été appelée.</span><span class="sxs-lookup"><span data-stu-id="879c2-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="879c2-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="879c2-128">Notes to callers</span></span>

<span data-ttu-id="879c2-129">Avant d’appeler **DeleteAttach**, appelez la méthode **IUnknown::Release** pour la pièce jointe et chacun de ses flux.</span><span class="sxs-lookup"><span data-stu-id="879c2-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="879c2-130">Étant donné que la suppression d’une pièce jointe peut être un processus long, **DeleteAttach** fournit le mécanisme qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="879c2-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="879c2-131">Vous pouvez demander l’affichage d’un indicateur de progression en passant un pointeur vers votre [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implémentation ou NULL si vous ne disposez pas d’une implémentation.</span><span class="sxs-lookup"><span data-stu-id="879c2-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="879c2-132">Vous devez également spécifier un handle de fenêtre dans le paramètre _ulUIParam_ et l’indicateur ATTACH_DIALOG dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="879c2-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="879c2-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="879c2-133">MFCMAPI reference</span></span>

<span data-ttu-id="879c2-134">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="879c2-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="879c2-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="879c2-135">**File**</span></span>|<span data-ttu-id="879c2-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="879c2-136">**Function**</span></span>|<span data-ttu-id="879c2-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="879c2-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="879c2-138">AttachmentsDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="879c2-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="879c2-139">CAttachmentsDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="879c2-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="879c2-140">MFCMAPI utilise la méthode **IMessage::DeleteAttach** pour supprimer la pièce jointe sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="879c2-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="879c2-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="879c2-141">See also</span></span>



[<span data-ttu-id="879c2-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="879c2-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="879c2-143">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="879c2-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="879c2-144">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="879c2-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

