---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417405"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="78182-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="78182-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="78182-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78182-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78182-105">Supprime un sous-foldeur.</span><span class="sxs-lookup"><span data-stu-id="78182-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="78182-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78182-106">Parameters</span></span>

 <span data-ttu-id="78182-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="78182-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="78182-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="78182-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="78182-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="78182-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="78182-110">[in] Pointeur vers l’identificateur d’entrée du sous-folder à supprimer.</span><span class="sxs-lookup"><span data-stu-id="78182-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="78182-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="78182-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="78182-112">[in] Handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="78182-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="78182-113">Le _paramètre ulUIParam_ est ignoré, sauf si l’FOLDER_DIALOG est définie dans _le paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="78182-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="78182-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="78182-114">_lpProgress_</span></span>
  
> <span data-ttu-id="78182-115">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="78182-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="78182-116">Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="78182-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="78182-117">Le  _paramètre lpProgress est_ ignoré, sauf si l’FOLDER_DIALOG est définie dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="78182-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="78182-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78182-118">_ulFlags_</span></span>
  
> <span data-ttu-id="78182-119">[in] Masque de bits d’indicateurs qui contrôle la suppression du sous-folder.</span><span class="sxs-lookup"><span data-stu-id="78182-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="78182-120">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="78182-120">The following flags can be set:</span></span>
    
<span data-ttu-id="78182-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="78182-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="78182-122">Tous les sous-fichiers du sous-fichier pointé par  _lpEntryID_ doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="78182-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="78182-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="78182-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="78182-124">Tous les messages dans le sous-fichier pointé par  _lpEntryID_ doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="78182-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="78182-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="78182-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="78182-126">Un indicateur de progression doit être affiché pendant la progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="78182-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78182-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="78182-127">Return value</span></span>

<span data-ttu-id="78182-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="78182-128">S_OK</span></span> 
  
> <span data-ttu-id="78182-129">Le dossier spécifié a été supprimé avec succès.</span><span class="sxs-lookup"><span data-stu-id="78182-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="78182-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="78182-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="78182-131">Le sous-fichier en cours de suppression contient des sous-DEL_FOLDERS et l’indicateur de DEL_FOLDERS n’a pas été définie.</span><span class="sxs-lookup"><span data-stu-id="78182-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="78182-132">Les sous-fichiers n’ont pas été supprimés.</span><span class="sxs-lookup"><span data-stu-id="78182-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="78182-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="78182-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="78182-134">Le sous-fichier supprimé contient des messages et l’DEL_MESSAGES n’a pas été définie.</span><span class="sxs-lookup"><span data-stu-id="78182-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="78182-135">Le sous-fichier n’a pas été supprimé.</span><span class="sxs-lookup"><span data-stu-id="78182-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="78182-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="78182-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="78182-137">L’appel a réussi, mais toutes les entrées n’ont pas été supprimées avec succès.</span><span class="sxs-lookup"><span data-stu-id="78182-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="78182-138">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="78182-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="78182-139">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="78182-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="78182-140">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="78182-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78182-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="78182-141">Remarks</span></span>

<span data-ttu-id="78182-142">La **méthode IMAPIFolder::D eleteFolder** supprime un sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="78182-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="78182-143">Par défaut, **DeleteFolder** fonctionne uniquement sur les dossiers vides, mais vous pouvez l’utiliser avec succès sur les dossiers non vides en fixant deux indicateurs : DEL_FOLDERS et DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="78182-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="78182-144">Seuls les dossiers vides ou les dossiers qui définissent les indicateurs DEL_FOLDERS et DEL_MESSAGES sur l’appel **DeleteFolder** peuvent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="78182-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="78182-145">DEL_FOLDERS tous les sous-dossiers du dossier peuvent être supprimés ; DEL_MESSAGES tous les messages du dossier peuvent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="78182-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="78182-146">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="78182-146">Notes to implementers</span></span>

<span data-ttu-id="78182-147">Lorsque l’opération de suppression implique plusieurs dossiers, effectuez l’opération aussi complètement que possible pour chaque dossier.</span><span class="sxs-lookup"><span data-stu-id="78182-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="78182-148">Parfois, l’un des dossiers à supprimer n’existe pas ou a été déplacé ou copié ailleurs.</span><span class="sxs-lookup"><span data-stu-id="78182-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="78182-149">N’arrêtez pas l’opération prématurément, sauf si une défaillance dépasse votre contrôle, par exemple un manque de mémoire, un manque d’espace disque ou une altération de la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="78182-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="78182-150">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="78182-150">Notes to callers</span></span>

<span data-ttu-id="78182-151">Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="78182-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="78182-152">**Condition**</span><span class="sxs-lookup"><span data-stu-id="78182-152">**Condition**</span></span>|<span data-ttu-id="78182-153">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="78182-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="78182-154">**DeleteFolder a** supprimé tous les messages et sous-fichiers avec succès.</span><span class="sxs-lookup"><span data-stu-id="78182-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="78182-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="78182-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="78182-156">**DeleteFolder n’a** pas pu supprimer tous les messages et sous-fichiers.</span><span class="sxs-lookup"><span data-stu-id="78182-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="78182-157">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="78182-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="78182-158">**DeleteFolder n’a** pas pu se terminer.</span><span class="sxs-lookup"><span data-stu-id="78182-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="78182-159">Toute valeur d’erreur à l’exception MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="78182-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="78182-160">Lorsque **DeleteFolder ne** parvient pas à se terminer, ne supposez pas qu’aucun travail n’a été effectué.</span><span class="sxs-lookup"><span data-stu-id="78182-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="78182-161">**DeleteFolder a** peut-être pu supprimer un ou plusieurs des messages et sous-fichiers avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="78182-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="78182-162">Si un ou plusieurs sous-fichiers ne peuvent pas être supprimés, **DeleteFolder** renvoie MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l’implémentation du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="78182-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="78182-163">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="78182-163">MFCMAPI reference</span></span>

<span data-ttu-id="78182-164">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="78182-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="78182-165">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="78182-165">**File**</span></span>|<span data-ttu-id="78182-166">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="78182-166">**Function**</span></span>|<span data-ttu-id="78182-167">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="78182-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78182-168">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="78182-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="78182-169">CMsgStoreDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="78182-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="78182-170">MFCMAPI utilise **la méthode IMAPIFolder::D eleteFolder** pour supprimer des dossiers.</span><span class="sxs-lookup"><span data-stu-id="78182-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78182-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78182-171">See also</span></span>



[<span data-ttu-id="78182-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="78182-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="78182-173">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="78182-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

