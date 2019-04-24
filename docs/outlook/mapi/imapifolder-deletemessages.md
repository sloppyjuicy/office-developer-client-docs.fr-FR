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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280119"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="20d8d-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="20d8d-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="20d8d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20d8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20d8d-105">Supprime un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="20d8d-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="20d8d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20d8d-106">Parameters</span></span>

 <span data-ttu-id="20d8d-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="20d8d-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="20d8d-108">dans Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient le nombre de messages à supprimer et un tableau de structures [EntryID](entryid.md) qui identifient les messages.</span><span class="sxs-lookup"><span data-stu-id="20d8d-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="20d8d-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="20d8d-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="20d8d-110">dans Handle de la fenêtre parent de l'indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="20d8d-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="20d8d-111">Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="20d8d-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="20d8d-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="20d8d-112">_lpProgress_</span></span>
  
> <span data-ttu-id="20d8d-113">dans Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="20d8d-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="20d8d-114">Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="20d8d-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="20d8d-115">Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="20d8d-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="20d8d-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20d8d-116">_ulFlags_</span></span>
  
> <span data-ttu-id="20d8d-117">dans Masque de des indicateurs qui contrôle la manière dont les messages sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="20d8d-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="20d8d-118">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="20d8d-118">The following flags can be set:</span></span>
    
<span data-ttu-id="20d8d-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="20d8d-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="20d8d-120">Supprime définitivement tous les messages, y compris ceux qui sont supprimés de manière récupérable.</span><span class="sxs-lookup"><span data-stu-id="20d8d-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="20d8d-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="20d8d-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="20d8d-122">Affiche un indicateur de progression pendant l'exécution de l'opération.</span><span class="sxs-lookup"><span data-stu-id="20d8d-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20d8d-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="20d8d-123">Return value</span></span>

<span data-ttu-id="20d8d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="20d8d-124">S_OK</span></span> 
  
> <span data-ttu-id="20d8d-125">Le ou les messages spécifiés ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="20d8d-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="20d8d-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="20d8d-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="20d8d-127">L'appel a réussi, mais tous les messages n'ont pas été supprimés.</span><span class="sxs-lookup"><span data-stu-id="20d8d-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="20d8d-128">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="20d8d-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="20d8d-129">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="20d8d-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="20d8d-130">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="20d8d-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20d8d-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="20d8d-131">Remarks</span></span>

<span data-ttu-id="20d8d-132">La méthode **IMAPIFolder::D eletemessages** supprime les messages d'un dossier.</span><span class="sxs-lookup"><span data-stu-id="20d8d-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="20d8d-133">Les messages qui n'existent pas, qui ont été déplacés ailleurs, qui sont ouverts avec une autorisation en lecture/écriture ou qui sont actuellement soumis, ne peuvent pas être supprimés.</span><span class="sxs-lookup"><span data-stu-id="20d8d-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="20d8d-134">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="20d8d-134">Notes to implementers</span></span>

<span data-ttu-id="20d8d-135">Lorsque l'opération de suppression implique plusieurs messages, effectuez l'opération aussi complètement que possible pour chaque dossier, même si un ou plusieurs messages ne peuvent pas être supprimés.</span><span class="sxs-lookup"><span data-stu-id="20d8d-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="20d8d-136">N'arrêtez pas l'opération prématurément à moins qu'une défaillance ne se produise au-delà de votre contrôle, telle qu'une mémoire insuffisante, un manque d'espace disque ou une corruption de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="20d8d-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="20d8d-137">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="20d8d-137">Notes to callers</span></span>

<span data-ttu-id="20d8d-138">Attendez-vous à ces valeurs de retour dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="20d8d-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="20d8d-139">**Condition**</span><span class="sxs-lookup"><span data-stu-id="20d8d-139">**Condition**</span></span>|<span data-ttu-id="20d8d-140">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="20d8d-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d8d-141">**DeleteMessages** a correctement supprimé tous les messages.</span><span class="sxs-lookup"><span data-stu-id="20d8d-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="20d8d-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="20d8d-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="20d8d-143">**DeleteMessages** n'a pas pu supprimer tous les messages et sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="20d8d-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="20d8d-144">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="20d8d-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="20d8d-145">**DeleteMessages** n'a pas pu être exécuté.</span><span class="sxs-lookup"><span data-stu-id="20d8d-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="20d8d-146">Toute valeur d'erreur à l'exception de MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="20d8d-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="20d8d-147">Lorsque **DeleteMessages** ne parvient pas à terminer, ne partez pas du principe qu'aucun travail n'a été effectué.</span><span class="sxs-lookup"><span data-stu-id="20d8d-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="20d8d-148">**DeleteMessages** a peut-être pu supprimer un ou plusieurs messages avant de rencontrer l'erreur.</span><span class="sxs-lookup"><span data-stu-id="20d8d-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="20d8d-149">**DeleteMessages** renvoie MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l'implémentation de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="20d8d-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="20d8d-150">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="20d8d-150">MFCMAPI reference</span></span>

<span data-ttu-id="20d8d-151">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="20d8d-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="20d8d-152">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="20d8d-152">**File**</span></span>|<span data-ttu-id="20d8d-153">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="20d8d-153">**Function**</span></span>|<span data-ttu-id="20d8d-154">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="20d8d-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="20d8d-155">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="20d8d-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="20d8d-156">CFolderDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="20d8d-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="20d8d-157">MFCMAPI utilise la méthode **IMAPIFolder::D eletemessages** pour supprimer les messages spécifiés.</span><span class="sxs-lookup"><span data-stu-id="20d8d-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20d8d-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20d8d-158">See also</span></span>



[<span data-ttu-id="20d8d-159">ENTRÉE</span><span class="sxs-lookup"><span data-stu-id="20d8d-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="20d8d-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="20d8d-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="20d8d-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="20d8d-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="20d8d-162">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="20d8d-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="20d8d-163">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="20d8d-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

