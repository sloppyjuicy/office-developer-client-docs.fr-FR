---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 287577babc9a40b771aa9917211ba5dcbf8190ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584939"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="9fe71-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="9fe71-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="9fe71-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fe71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fe71-105">Supprime tous les messages et les sous-dossiers d’un dossier sans supprimer le dossier proprement dit.</span><span class="sxs-lookup"><span data-stu-id="9fe71-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9fe71-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fe71-106">Parameters</span></span>

 <span data-ttu-id="9fe71-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9fe71-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="9fe71-108">[in] Un handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="9fe71-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="9fe71-109">Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9fe71-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9fe71-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9fe71-110">_lpProgress_</span></span>
  
> <span data-ttu-id="9fe71-111">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="9fe71-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9fe71-112">Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="9fe71-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="9fe71-113">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9fe71-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9fe71-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9fe71-114">_ulFlags_</span></span>
  
> <span data-ttu-id="9fe71-115">[in] Masque de bits d’indicateurs qui contrôle la façon dont le dossier est vidé.</span><span class="sxs-lookup"><span data-stu-id="9fe71-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="9fe71-116">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="9fe71-116">The following flags can be set:</span></span>
    
<span data-ttu-id="9fe71-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="9fe71-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="9fe71-118">Supprime tous les sous-dossiers, y compris les sous-dossiers qui contiennent des messages avec contenu associé.</span><span class="sxs-lookup"><span data-stu-id="9fe71-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="9fe71-119">L’indicateur DEL_ASSOCIATED a de signification seulement pour l’appel agit sur le dossier de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="9fe71-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="9fe71-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="9fe71-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="9fe71-121">Supprime définitivement tous les messages, y compris ceux récupérable.</span><span class="sxs-lookup"><span data-stu-id="9fe71-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="9fe71-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9fe71-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="9fe71-123">Affiche un indicateur de progression pendant que l’opération s’effectue.</span><span class="sxs-lookup"><span data-stu-id="9fe71-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9fe71-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="9fe71-124">Return value</span></span>

<span data-ttu-id="9fe71-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="9fe71-125">S_OK</span></span> 
  
> <span data-ttu-id="9fe71-126">Le dossier a été vidé avec succès.</span><span class="sxs-lookup"><span data-stu-id="9fe71-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="9fe71-127">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="9fe71-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="9fe71-128">L’appel a réussi, mais le dossier n’a pas été vidé complètement.</span><span class="sxs-lookup"><span data-stu-id="9fe71-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="9fe71-129">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="9fe71-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="9fe71-130">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="9fe71-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9fe71-131">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="9fe71-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9fe71-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="9fe71-132">Remarks</span></span>

<span data-ttu-id="9fe71-133">La méthode **IMAPIFolder::EmptyFolder** supprime tout contenu d’un dossier sans supprimer le dossier proprement dit.</span><span class="sxs-lookup"><span data-stu-id="9fe71-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="9fe71-134">Pendant un appel **EmptyFolder** , les messages envoyés ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="9fe71-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="9fe71-135">Contenu associé d’un dossier comprennent les messages qui sont utilisés pour décrire les affichages, les règles, les formulaires personnalisés et du stockage des solutions personnalisées et peuvent également inclure des définitions de formulaire.</span><span class="sxs-lookup"><span data-stu-id="9fe71-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9fe71-136">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="9fe71-136">Notes to implementers</span></span>

<span data-ttu-id="9fe71-137">N’appelez pas la méthode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour les messages qui ont été envoyés dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="9fe71-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="9fe71-138">Les messages envoyés ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="9fe71-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9fe71-139">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="9fe71-139">Notes to callers</span></span>

<span data-ttu-id="9fe71-140">Prévoyez ces valeurs de retour dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="9fe71-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="9fe71-141">**Condition**</span><span class="sxs-lookup"><span data-stu-id="9fe71-141">**Condition**</span></span>|<span data-ttu-id="9fe71-142">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="9fe71-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9fe71-143">**EmptyFolder** a vidé avec succès le dossier.</span><span class="sxs-lookup"><span data-stu-id="9fe71-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="9fe71-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="9fe71-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="9fe71-145">**EmptyFolder** n’a pas pu vider entièrement le dossier.</span><span class="sxs-lookup"><span data-stu-id="9fe71-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="9fe71-146">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="9fe71-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="9fe71-147">**EmptyFolder** n’a pas pu terminer.</span><span class="sxs-lookup"><span data-stu-id="9fe71-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="9fe71-148">Une valeur d’erreur</span><span class="sxs-lookup"><span data-stu-id="9fe71-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="9fe71-149">Lorsque **EmptyFolder** n’aboutit pas, ne supposez pas qu’aucun travail n’a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="9fe71-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="9fe71-150">**EmptyFolder** peut-être en mesure de supprimer le contenu du dossier avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="9fe71-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9fe71-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9fe71-151">MFCMAPI reference</span></span>

<span data-ttu-id="9fe71-152">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9fe71-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9fe71-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="9fe71-153">**File**</span></span>|<span data-ttu-id="9fe71-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="9fe71-154">**Function**</span></span>|<span data-ttu-id="9fe71-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="9fe71-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9fe71-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9fe71-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="9fe71-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="9fe71-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="9fe71-158">MFCMAPI utilise la méthode **IMAPIFolder::EmptyFolder** pour supprimer le contenu du dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="9fe71-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fe71-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fe71-159">See also</span></span>



[<span data-ttu-id="9fe71-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="9fe71-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="9fe71-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9fe71-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="9fe71-162">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="9fe71-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="9fe71-163">Utilisation des macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="9fe71-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

