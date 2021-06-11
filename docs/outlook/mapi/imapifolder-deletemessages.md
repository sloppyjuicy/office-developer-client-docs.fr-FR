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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426071"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="a3f30-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="a3f30-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="a3f30-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3f30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3f30-105">Supprime un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="a3f30-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a3f30-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a3f30-106">Parameters</span></span>

 <span data-ttu-id="a3f30-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="a3f30-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="a3f30-108">[in] Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient le nombre de messages à supprimer et un tableau de structures [ENTRYID](entryid.md) qui identifient les messages.</span><span class="sxs-lookup"><span data-stu-id="a3f30-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="a3f30-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a3f30-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="a3f30-110">[in] Handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="a3f30-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="a3f30-111">Le _paramètre ulUIParam_ est ignoré, sauf si l’MESSAGE_DIALOG est définie dans _le paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a3f30-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a3f30-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a3f30-112">_lpProgress_</span></span>
  
> <span data-ttu-id="a3f30-113">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="a3f30-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a3f30-114">Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="a3f30-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="a3f30-115">Le _paramètre lpProgress est_ ignoré, sauf si l’MESSAGE_DIALOG est définie dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a3f30-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a3f30-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3f30-116">_ulFlags_</span></span>
  
> <span data-ttu-id="a3f30-117">[in] Masque de bits d’indicateurs qui contrôle la façon dont les messages sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="a3f30-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="a3f30-118">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="a3f30-118">The following flags can be set:</span></span>
    
<span data-ttu-id="a3f30-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="a3f30-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="a3f30-120">Supprime définitivement tous les messages, y compris les messages supprimés (supprimés de manière temporaire).</span><span class="sxs-lookup"><span data-stu-id="a3f30-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="a3f30-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a3f30-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="a3f30-122">Affiche un indicateur de progression au cours de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a3f30-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3f30-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a3f30-123">Return value</span></span>

<span data-ttu-id="a3f30-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3f30-124">S_OK</span></span> 
  
> <span data-ttu-id="a3f30-125">Le ou les messages spécifiés ont été supprimés avec succès.</span><span class="sxs-lookup"><span data-stu-id="a3f30-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="a3f30-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a3f30-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="a3f30-127">L’appel a réussi, mais tous les messages n’ont pas été supprimés avec succès.</span><span class="sxs-lookup"><span data-stu-id="a3f30-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="a3f30-128">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="a3f30-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a3f30-129">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="a3f30-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a3f30-130">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="a3f30-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3f30-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3f30-131">Remarks</span></span>

<span data-ttu-id="a3f30-132">La **méthode IMAPIFolder::D eleteMessages** supprime les messages d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="a3f30-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="a3f30-133">Les messages qui n’existent pas, qui ont été déplacés ailleurs, qui sont ouverts avec une autorisation de lecture/écriture ou qui sont actuellement envoyés ne peuvent pas être supprimés.</span><span class="sxs-lookup"><span data-stu-id="a3f30-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a3f30-134">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a3f30-134">Notes to implementers</span></span>

<span data-ttu-id="a3f30-135">Lorsque l’opération de suppression implique plusieurs messages, effectuez l’opération aussi complètement que possible pour chaque dossier, même si un ou plusieurs des messages ne peuvent pas être supprimés.</span><span class="sxs-lookup"><span data-stu-id="a3f30-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="a3f30-136">N’arrêtez pas l’opération prématurément, sauf si une défaillance dépasse votre contrôle, par exemple un manque de mémoire, un manque d’espace disque ou une altération de la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="a3f30-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3f30-137">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="a3f30-137">Notes to callers</span></span>

<span data-ttu-id="a3f30-138">Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3f30-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="a3f30-139">**Condition**</span><span class="sxs-lookup"><span data-stu-id="a3f30-139">**Condition**</span></span>|<span data-ttu-id="a3f30-140">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="a3f30-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3f30-141">**DeleteMessages a** correctement supprimé chaque message.</span><span class="sxs-lookup"><span data-stu-id="a3f30-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="a3f30-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3f30-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="a3f30-143">**DeleteMessages n’a** pas pu supprimer correctement tous les messages et sous-fichiers.</span><span class="sxs-lookup"><span data-stu-id="a3f30-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="a3f30-144">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a3f30-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="a3f30-145">**DeleteMessages** n’a pas pu se terminer.</span><span class="sxs-lookup"><span data-stu-id="a3f30-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="a3f30-146">Toute valeur d’erreur à l’exception MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a3f30-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="a3f30-147">Lorsque **DeleteMessages n’est** pas en mesure de se terminer, ne supposez pas qu’aucun travail n’a été effectué.</span><span class="sxs-lookup"><span data-stu-id="a3f30-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="a3f30-148">**DeleteMessages a** peut-être pu supprimer un ou plusieurs des messages avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a3f30-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="a3f30-149">**DeleteMessages renvoie** MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l’implémentation de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="a3f30-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a3f30-150">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a3f30-150">MFCMAPI reference</span></span>

<span data-ttu-id="a3f30-151">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a3f30-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a3f30-152">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="a3f30-152">**File**</span></span>|<span data-ttu-id="a3f30-153">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a3f30-153">**Function**</span></span>|<span data-ttu-id="a3f30-154">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a3f30-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a3f30-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a3f30-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="a3f30-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="a3f30-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="a3f30-157">MFCMAPI utilise **la méthode IMAPIFolder::D eleteMessages** pour supprimer les messages spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a3f30-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3f30-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3f30-158">See also</span></span>



[<span data-ttu-id="a3f30-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a3f30-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="a3f30-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="a3f30-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="a3f30-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a3f30-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="a3f30-162">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="a3f30-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a3f30-163">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="a3f30-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

