---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bd0439c71df7083e3c4787a5d317fa11d2b99c61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578632"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="abf66-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="abf66-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="abf66-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abf66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abf66-105">Supprime un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="abf66-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="abf66-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abf66-106">Parameters</span></span>

 <span data-ttu-id="abf66-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="abf66-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="abf66-108">[in] Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient le nombre de messages à supprimer et un tableau de structures [ENTRYID](entryid.md) qui identifient les messages.</span><span class="sxs-lookup"><span data-stu-id="abf66-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="abf66-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="abf66-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="abf66-110">[in] Un handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="abf66-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="abf66-111">Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="abf66-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="abf66-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="abf66-112">_lpProgress_</span></span>
  
> <span data-ttu-id="abf66-113">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="abf66-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="abf66-114">Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="abf66-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="abf66-115">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="abf66-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="abf66-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="abf66-116">_ulFlags_</span></span>
  
> <span data-ttu-id="abf66-117">[in] Masque de bits d’indicateurs qui contrôle la façon dont les messages sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="abf66-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="abf66-118">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="abf66-118">The following flags can be set:</span></span>
    
<span data-ttu-id="abf66-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="abf66-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="abf66-120">Supprime définitivement tous les messages, y compris ceux récupérable.</span><span class="sxs-lookup"><span data-stu-id="abf66-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="abf66-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="abf66-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="abf66-122">Affiche un indicateur de progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="abf66-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="abf66-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="abf66-123">Return value</span></span>

<span data-ttu-id="abf66-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="abf66-124">S_OK</span></span> 
  
> <span data-ttu-id="abf66-125">L’ou les messages spécifié ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="abf66-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="abf66-126">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="abf66-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="abf66-127">L’appel a réussi, mais pas tous les messages ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="abf66-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="abf66-128">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="abf66-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="abf66-129">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="abf66-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="abf66-130">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="abf66-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="abf66-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="abf66-131">Remarks</span></span>

<span data-ttu-id="abf66-132">La méthode **IMAPIFolder::DeleteMessages** supprime les messages à partir d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="abf66-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="abf66-133">Impossible de supprimer les messages qui n’existent pas, qui ont été déplacés ailleurs, qui sont ouverts avec l’autorisation de lecture/écriture ou qui sont actuellement soumis.</span><span class="sxs-lookup"><span data-stu-id="abf66-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="abf66-134">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="abf66-134">Notes to implementers</span></span>

<span data-ttu-id="abf66-135">Lorsque l’opération de suppression implique plusieurs messages, effectuer l’opération complètement que possible pour chaque dossier, même si un ou plusieurs des messages ne peuvent pas être supprimées.</span><span class="sxs-lookup"><span data-stu-id="abf66-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="abf66-136">N’arrêtez pas l’opération prématurément, sauf si une panne se produit qui est votre volonté, telles que le manque de mémoire, manque d’espace disque ou l’endommagement de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="abf66-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="abf66-137">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="abf66-137">Notes to callers</span></span>

<span data-ttu-id="abf66-138">Prévoyez ces valeurs de retour dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="abf66-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="abf66-139">**Condition**</span><span class="sxs-lookup"><span data-stu-id="abf66-139">**Condition**</span></span>|<span data-ttu-id="abf66-140">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="abf66-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abf66-141">**DeleteMessages** a supprimé tous les messages.</span><span class="sxs-lookup"><span data-stu-id="abf66-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="abf66-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="abf66-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="abf66-143">Impossible de supprimer tous les messages et sous-dossier **DeleteMessages** .</span><span class="sxs-lookup"><span data-stu-id="abf66-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="abf66-144">MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="abf66-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="abf66-145">**DeleteMessages** n’a pas pu terminer.</span><span class="sxs-lookup"><span data-stu-id="abf66-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="abf66-146">Une valeur d’erreur à l’exception MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="abf66-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="abf66-147">Lorsque **DeleteMessages** n’aboutit pas, ne supposez pas qu’aucun travail n’a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="abf66-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="abf66-148">**DeleteMessages** peut-être en mesure de supprimer un ou plusieurs des messages avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="abf66-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="abf66-149">**DeleteMessages** renvoie MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND, en fonction de l’implémentation de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="abf66-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="abf66-150">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="abf66-150">MFCMAPI reference</span></span>

<span data-ttu-id="abf66-151">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="abf66-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="abf66-152">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="abf66-152">**File**</span></span>|<span data-ttu-id="abf66-153">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="abf66-153">**Function**</span></span>|<span data-ttu-id="abf66-154">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="abf66-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="abf66-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="abf66-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="abf66-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="abf66-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="abf66-157">MFCMAPI utilise la méthode **IMAPIFolder::DeleteMessages** pour supprimer les messages spécifiés.</span><span class="sxs-lookup"><span data-stu-id="abf66-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abf66-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abf66-158">See also</span></span>



[<span data-ttu-id="abf66-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="abf66-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="abf66-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="abf66-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="abf66-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="abf66-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="abf66-162">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="abf66-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="abf66-163">Utilisation des macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="abf66-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

