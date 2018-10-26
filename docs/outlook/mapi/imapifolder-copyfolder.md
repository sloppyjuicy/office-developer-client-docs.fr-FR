---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 134a492dbc86dd0ce6b3795d5ae40b334c14d468
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585149"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="b41f4-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="b41f4-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="b41f4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b41f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b41f4-105">Copie ou déplace un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="b41f4-105">Copies or moves a subfolder.</span></span>
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b41f4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b41f4-106">Parameters</span></span>

 <span data-ttu-id="b41f4-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b41f4-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b41f4-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b41f4-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b41f4-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b41f4-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b41f4-110">[in] Pointeur vers l’identificateur d’entrée du sous-dossier pour copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="b41f4-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="b41f4-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b41f4-111">_lpInterface_</span></span>
  
> <span data-ttu-id="b41f4-112">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au dossier vers lequel pointe le paramètre _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="b41f4-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="b41f4-113">Passage de NULL entraîne le fournisseur de services renvoyer l’interface dossier standard, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b41f4-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="b41f4-114">Les valeurs valides pour _lpInterface_ sont IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="b41f4-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="b41f4-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="b41f4-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="b41f4-116">[in] Pointeur vers le dossier ouvert pour recevoir le sous-dossier copié ou déplacé.</span><span class="sxs-lookup"><span data-stu-id="b41f4-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="b41f4-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="b41f4-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="b41f4-118">[in] Pointeur vers le nom du dossier copié ou déplacé dans son nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="b41f4-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="b41f4-119">Si _lpszNewFolderName_ est défini sur NULL, le nom du sous-dossier source est utilisé pour le nom du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="b41f4-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="b41f4-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b41f4-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="b41f4-121">[in] Un handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="b41f4-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="b41f4-122">Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur FOLDER_DIALOG dans le paramètre _ulFlags_ est défini.</span><span class="sxs-lookup"><span data-stu-id="b41f4-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="b41f4-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="b41f4-123">_lpProgress_</span></span>
  
> <span data-ttu-id="b41f4-124">[in] Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="b41f4-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="b41f4-125">Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="b41f4-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="b41f4-126">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="b41f4-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="b41f4-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b41f4-127">_ulFlags_</span></span>
  
> <span data-ttu-id="b41f4-128">[in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="b41f4-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="b41f4-129">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="b41f4-129">The following flags can be set:</span></span>
    
<span data-ttu-id="b41f4-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="b41f4-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="b41f4-131">Tous les sous-dossiers dans le sous-dossier à copier doivent également être copiés.</span><span class="sxs-lookup"><span data-stu-id="b41f4-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="b41f4-132">Lorsque COPY_SUBFOLDERS n’est pas définie pour une opération de copie, uniquement dans le sous-dossier identifié par _lpEntryID_ est copié.</span><span class="sxs-lookup"><span data-stu-id="b41f4-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="b41f4-133">Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est la valeur par défaut que si l’indicateur est défini.</span><span class="sxs-lookup"><span data-stu-id="b41f4-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="b41f4-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b41f4-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="b41f4-135">Demande l’affichage d’un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="b41f4-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="b41f4-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="b41f4-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="b41f4-137">Le sous-dossier doit être déplacé au lieu de copier.</span><span class="sxs-lookup"><span data-stu-id="b41f4-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="b41f4-138">Si FOLDER_MOVE n’est pas défini, le sous-dossier est copié.</span><span class="sxs-lookup"><span data-stu-id="b41f4-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="b41f4-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="b41f4-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="b41f4-140">Informe le fournisseur de banque de messages que s’il implémente **CopyFolder** en appelant la méthode [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) de l’objet de la prise en charge, **CopyFolder** doit retourner à la place immédiatement MAPI_E_ DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="b41f4-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="b41f4-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b41f4-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b41f4-142">Le nom du dossier de destination est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="b41f4-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="b41f4-143">Si l’indicateur MAPI_UNICODE n’est pas définie, le nom du dossier est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="b41f4-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b41f4-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b41f4-144">Return value</span></span>

<span data-ttu-id="b41f4-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="b41f4-145">S_OK</span></span> 
  
> <span data-ttu-id="b41f4-146">Le dossier spécifié a été copié ou déplacé.</span><span class="sxs-lookup"><span data-stu-id="b41f4-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="b41f4-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b41f4-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b41f4-148">Soit l’indicateur MAPI_UNICODE a été défini et le fournisseur de banque de messages ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et prend en charge le fournisseur de banque de message Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="b41f4-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="b41f4-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="b41f4-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="b41f4-150">Le nom du dossier en cours de déplacer ou copier est la même que celle d’un sous-dossier dans le dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="b41f4-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="b41f4-151">Le fournisseur de banque de messages exige que les noms de dossier unique.</span><span class="sxs-lookup"><span data-stu-id="b41f4-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="b41f4-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="b41f4-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="b41f4-153">Le fournisseur implémente cette méthode en appelant une méthode de prise en charge de l’objet et l’appelant a passé l’indicateur MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="b41f4-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="b41f4-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="b41f4-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="b41f4-155">Le dossier source, directement ou indirectement contient le dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="b41f4-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="b41f4-156">Travail significatifs a peut-être été effectué avant cette condition a été détectée, le dossier source et de destination peut être modifié partiellement.</span><span class="sxs-lookup"><span data-stu-id="b41f4-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="b41f4-157">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="b41f4-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="b41f4-158">L’appel a réussi, mais pas toutes les entrées ont été correctement copiées.</span><span class="sxs-lookup"><span data-stu-id="b41f4-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="b41f4-159">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="b41f4-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b41f4-160">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="b41f4-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b41f4-161">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b41f4-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b41f4-162">Remarques</span><span class="sxs-lookup"><span data-stu-id="b41f4-162">Remarks</span></span>

<span data-ttu-id="b41f4-163">La méthode **IMAPIFolder::CopyFolder** copie ou déplace un sous-dossier d’un emplacement vers un autre.</span><span class="sxs-lookup"><span data-stu-id="b41f4-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="b41f4-164">Le sous-dossier copiées ou déplacées est ajouté au dossier de destination, comme un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="b41f4-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b41f4-165">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b41f4-165">Notes to implementers</span></span>

<span data-ttu-id="b41f4-166">Lorsque l’opération de copie ou de déplacement implique plusieurs dossiers, comme indiqué par l’indicateur COPY_SUBFOLDERS, effectuez l’opération complètement que possible pour chaque dossier.</span><span class="sxs-lookup"><span data-stu-id="b41f4-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="b41f4-167">Parfois, un des dossiers d’être déplacé ou copié n’existe pas ou a déjà été déplacé ou copié ailleurs.</span><span class="sxs-lookup"><span data-stu-id="b41f4-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="b41f4-168">N’arrêtez pas l’opération prématurément, sauf si une panne se produit qui est votre volonté, telles que le manque de mémoire, manque d’espace disque ou l’endommagement de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="b41f4-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="b41f4-169">Essayez de conserver tous les identificateurs d’entrée de message dans les messages copiés.</span><span class="sxs-lookup"><span data-stu-id="b41f4-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="b41f4-170">Vous devriez également conserver les identificateurs d’entrée, mais il n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b41f4-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b41f4-171">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="b41f4-171">Notes to callers</span></span>

<span data-ttu-id="b41f4-172">Prévoyez ces valeurs de retour dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b41f4-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="b41f4-173">**Condition**</span><span class="sxs-lookup"><span data-stu-id="b41f4-173">**Condition**</span></span>|<span data-ttu-id="b41f4-174">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="b41f4-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b41f4-175">**CopyFolder** a été copié ou déplacé tous les messages et sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="b41f4-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="b41f4-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="b41f4-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="b41f4-177">**CopyFolder** n’a pas pu copier ou déplacer tous les messages et sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="b41f4-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="b41f4-178">MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b41f4-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="b41f4-179">**CopyFolder** n’a pas pu terminer.</span><span class="sxs-lookup"><span data-stu-id="b41f4-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="b41f4-180">Une valeur d’erreur à l’exception MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b41f4-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="b41f4-181">Lorsque **CopyFolder** n’aboutit pas, ne supposez pas qu’aucun travail n’a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b41f4-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="b41f4-182">**CopyFolder** peut-être en mesure de copier ou déplacer une ou plusieurs des messages et les sous-dossiers avant de rencontrer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b41f4-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="b41f4-183">Si un identificateur pour un dossier qui n’existe pas d’entrée est passé dans _lpEntryID_, **CopyFolder** renvoie MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND, en fonction de l’implémentation de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="b41f4-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="b41f4-184">Selon le fournisseur de banque de message, l’identificateur d’entrée du message d’origine peut-être ou ne peut pas être conservé dans le message copié.</span><span class="sxs-lookup"><span data-stu-id="b41f4-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="b41f4-185">Vous devez conserver les identificateurs d’entrée la mesure du possible, mais il n’est pas une condition requise.</span><span class="sxs-lookup"><span data-stu-id="b41f4-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="b41f4-186">Vous pouvez généralement dépendent les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="b41f4-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="b41f4-187">Lorsque vous déplacez un dossier entre les deux types de banques de messages, l’identificateur d’entrée est garanti à modifier.</span><span class="sxs-lookup"><span data-stu-id="b41f4-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="b41f4-188">Lorsque vous déplacez un dossier entre deux bases de messages du même type, l’identificateur d’entrée change presque toujours.</span><span class="sxs-lookup"><span data-stu-id="b41f4-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="b41f4-189">Lorsque vous déplacez un dossier à un autre emplacement dans le même magasin de message, l’identificateur d’entrée peut ou ne peut-être pas modifier, selon le message le fournisseur de magasins.</span><span class="sxs-lookup"><span data-stu-id="b41f4-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="b41f4-190">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b41f4-190">MFCMAPI reference</span></span>

<span data-ttu-id="b41f4-191">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b41f4-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b41f4-192">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="b41f4-192">**File**</span></span>|<span data-ttu-id="b41f4-193">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="b41f4-193">**Function**</span></span>|<span data-ttu-id="b41f4-194">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="b41f4-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b41f4-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b41f4-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="b41f4-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="b41f4-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="b41f4-197">MFCMAPI utilise la méthode **IMAPIFolder::CopyFolder** pour copier des dossiers d’un emplacement vers un autre.</span><span class="sxs-lookup"><span data-stu-id="b41f4-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="b41f4-198">MFCMAPI mémorise le dossier source pendant l’opération de copie et effectue la copie pendant l’opération de collage.</span><span class="sxs-lookup"><span data-stu-id="b41f4-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b41f4-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b41f4-199">See also</span></span>



[<span data-ttu-id="b41f4-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b41f4-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="b41f4-201">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="b41f4-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

