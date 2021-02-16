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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416782"
---
# <a name="imapifolderemptyfolder"></a><span data-ttu-id="84591-103">IMAPIFolder::EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="84591-103">IMAPIFolder::EmptyFolder</span></span>

  
  
<span data-ttu-id="84591-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84591-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84591-105">Supprime tous les messages et sous-dossiers d’un dossier sans supprimer le dossier lui-même.</span><span class="sxs-lookup"><span data-stu-id="84591-105">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="84591-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84591-106">Parameters</span></span>

 <span data-ttu-id="84591-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="84591-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="84591-108">[in] Handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="84591-108">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="84591-109">Le _paramètre ulUIParam_ est ignoré, sauf si l’FOLDER_DIALOG est définie dans _le paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="84591-109">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="84591-110">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="84591-110">_lpProgress_</span></span>
  
> <span data-ttu-id="84591-111">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="84591-111">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="84591-112">Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="84591-112">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="84591-113">Le _paramètre lpProgress est_ ignoré, sauf si l’FOLDER_DIALOG est définie dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="84591-113">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="84591-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="84591-114">_ulFlags_</span></span>
  
> <span data-ttu-id="84591-115">[in] Masque de bits d’indicateurs qui contrôle la façon dont le dossier est vidé.</span><span class="sxs-lookup"><span data-stu-id="84591-115">[in] A bitmask of flags that controls how the folder is emptied.</span></span> <span data-ttu-id="84591-116">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="84591-116">The following flags can be set:</span></span>
    
<span data-ttu-id="84591-117">DEL_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="84591-117">DEL_ASSOCIATED</span></span> 
  
> <span data-ttu-id="84591-118">Supprime tous les sous-fichiers, y compris les sous-fichiers qui contiennent des messages avec le contenu associé.</span><span class="sxs-lookup"><span data-stu-id="84591-118">Deletes all subfolders, including subfolders that contain messages with associated content.</span></span> <span data-ttu-id="84591-119">L DEL_ASSOCIATED’indicateur n’a de signification que pour le dossier de niveau supérieur sur qui l’appel agit.</span><span class="sxs-lookup"><span data-stu-id="84591-119">The DEL_ASSOCIATED flag has meaning only for the top-level folder the call acts on.</span></span>
    
<span data-ttu-id="84591-120">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="84591-120">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="84591-121">Supprime définitivement tous les messages, y compris les messages supprimés (supprimés de manière temporaire).</span><span class="sxs-lookup"><span data-stu-id="84591-121">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="84591-122">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="84591-122">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="84591-123">Affiche un indicateur de progression pendant la progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="84591-123">Displays a progress indicator while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84591-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84591-124">Return value</span></span>

<span data-ttu-id="84591-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="84591-125">S_OK</span></span> 
  
> <span data-ttu-id="84591-126">Le dossier a été vidé.</span><span class="sxs-lookup"><span data-stu-id="84591-126">The folder was successfully emptied.</span></span>
    
<span data-ttu-id="84591-127">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="84591-127">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="84591-128">L’appel a réussi, mais le dossier n’a pas été complètement vidé.</span><span class="sxs-lookup"><span data-stu-id="84591-128">The call succeeded, but the folder was not completely emptied.</span></span> <span data-ttu-id="84591-129">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="84591-129">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="84591-130">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="84591-130">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="84591-131">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="84591-131">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84591-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="84591-132">Remarks</span></span>

<span data-ttu-id="84591-133">La **méthode IMAPIFolder::EmptyFolder** supprime tout le contenu d’un dossier sans supprimer le dossier lui-même.</span><span class="sxs-lookup"><span data-stu-id="84591-133">The **IMAPIFolder::EmptyFolder** method deletes all of a folder's contents without deleting the folder itself.</span></span> 
  
<span data-ttu-id="84591-134">Pendant un **appel EmptyFolder,** les messages envoyés ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="84591-134">During an **EmptyFolder** call, submitted messages are not deleted.</span></span> 
  
<span data-ttu-id="84591-135">Le contenu associé à un dossier inclut des messages qui sont utilisés pour décrire les affichages, les règles, les formulaires personnalisés et le stockage de solutions personnalisées, et peut également inclure des définitions de formulaire.</span><span class="sxs-lookup"><span data-stu-id="84591-135">A folder's associated contents include messages that are used to describe views, rules, custom forms, and custom solution storage, and can also include form definitions.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="84591-136">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="84591-136">Notes to implementers</span></span>

<span data-ttu-id="84591-137">N’appelez [pas la méthode IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour les messages dans le dossier qui ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="84591-137">Do not call the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method for messages in the folder that have been submitted.</span></span> <span data-ttu-id="84591-138">Les messages envoyés ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="84591-138">Submitted messages are not deleted.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="84591-139">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="84591-139">Notes to callers</span></span>

<span data-ttu-id="84591-140">Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="84591-140">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="84591-141">**Condition**</span><span class="sxs-lookup"><span data-stu-id="84591-141">**Condition**</span></span>|<span data-ttu-id="84591-142">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="84591-142">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="84591-143">**EmptyFolder a** correctement vidé le dossier.</span><span class="sxs-lookup"><span data-stu-id="84591-143">**EmptyFolder** has successfully emptied the folder.</span></span>  <br/> |<span data-ttu-id="84591-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="84591-144">S_OK</span></span>  <br/> |
|<span data-ttu-id="84591-145">**EmptyFolder n’a** pas pu vider complètement le dossier.</span><span class="sxs-lookup"><span data-stu-id="84591-145">**EmptyFolder** was unable to completely empty the folder.</span></span>  <br/> |<span data-ttu-id="84591-146">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="84591-146">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="84591-147">**EmptyFolder n’a** pas pu se terminer.</span><span class="sxs-lookup"><span data-stu-id="84591-147">**EmptyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="84591-148">Toute valeur d’erreur</span><span class="sxs-lookup"><span data-stu-id="84591-148">Any error value</span></span>  <br/> |
   
<span data-ttu-id="84591-149">Lorsque **EmptyFolder ne** parvient pas à se terminer, ne supposez pas qu’aucun travail n’a été effectué.</span><span class="sxs-lookup"><span data-stu-id="84591-149">When **EmptyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="84591-150">**EmptyFolder a** peut-être pu supprimer une partie du contenu du dossier avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="84591-150">**EmptyFolder** might have been able to delete some of the folder's contents before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="84591-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="84591-151">MFCMAPI reference</span></span>

<span data-ttu-id="84591-152">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="84591-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="84591-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="84591-153">**File**</span></span>|<span data-ttu-id="84591-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="84591-154">**Function**</span></span>|<span data-ttu-id="84591-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="84591-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84591-156">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="84591-156">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="84591-157">CMsgStoreDlg::OnEmptyFolder</span><span class="sxs-lookup"><span data-stu-id="84591-157">CMsgStoreDlg::OnEmptyFolder</span></span>  <br/> |<span data-ttu-id="84591-158">MFCMAPI utilise la **méthode IMAPIFolder::EmptyFolder** pour supprimer le contenu du dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="84591-158">MFCMAPI uses the **IMAPIFolder::EmptyFolder** method to delete the contents of the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84591-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84591-159">See also</span></span>



[<span data-ttu-id="84591-160">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="84591-160">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="84591-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="84591-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="84591-162">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="84591-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="84591-163">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="84591-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

