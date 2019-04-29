---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420884"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="2ff2e-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="2ff2e-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="2ff2e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ff2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ff2e-105">Copie ou déplace un dossier à partir de son dossier parent actuel vers un autre dossier parent.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
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

## <a name="parameters"></a><span data-ttu-id="2ff2e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ff2e-106">Parameters</span></span>

 <span data-ttu-id="2ff2e-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="2ff2e-108">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au dossier parent du dossier à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="2ff2e-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="2ff2e-110">dans Pointeur vers le dossier parent du dossier à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="2ff2e-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="2ff2e-112">dans Nombre d'octets dans l'identificateur d'entrée pointé par _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="2ff2e-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="2ff2e-114">dans Pointeur vers l'identificateur d'entrée du dossier à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="2ff2e-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-115">_lpInterface_</span></span>
  
> <span data-ttu-id="2ff2e-116">dans MSR doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="2ff2e-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="2ff2e-118">dans Pointeur vers le dossier qui doit recevoir le dossier à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="2ff2e-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="2ff2e-120">dans Pointeur vers le nom du dossier copié ou déplacé; Sinon, NULL, ce qui indique que le dossier copié ou déplacé doit avoir le même nom que le dossier source (le dossier pointé par _lpEntryID_).</span><span class="sxs-lookup"><span data-stu-id="2ff2e-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="2ff2e-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="2ff2e-122">dans Handle de la fenêtre de la boîte de dialogue indicateur de progression et fenêtres associées.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="2ff2e-123">Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="2ff2e-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2ff2e-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-124">_lpProgress_</span></span>
  
> <span data-ttu-id="2ff2e-125">dans Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="2ff2e-126">Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="2ff2e-127">Le paramètre _lpProgress_ est ignoré sauf si l'indicateur FOLDER_DIALOG est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="2ff2e-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ff2e-128">_ulFlags_</span></span>
  
> <span data-ttu-id="2ff2e-129">dans Masque de des indicateurs qui contrôle le mode d'exécution de l'opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="2ff2e-130">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="2ff2e-130">The following flags can be set:</span></span>
    
<span data-ttu-id="2ff2e-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="2ff2e-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="2ff2e-132">Tous les sous-dossiers du dossier doivent être copiés ou déplacés.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="2ff2e-133">Lorsque COPY_SUBFOLDERS n'est pas défini pour une opération de copie, seul le dossier identifié par _lpEntryID_ est copié.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="2ff2e-134">Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est la valeur par défaut, que l'indicateur soit défini ou non.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="2ff2e-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2ff2e-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="2ff2e-136">Demande l'affichage d'un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="2ff2e-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="2ff2e-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="2ff2e-138">Le dossier doit être déplacé au lieu d'être copié.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="2ff2e-139">Si FOLDER_MOVE n'est pas défini, le dossier est copié.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="2ff2e-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ff2e-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2ff2e-141">Le nom du dossier est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="2ff2e-142">Si l'indicateur MAPI_UNICODE n'est pas défini, le nom du dossier est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ff2e-143">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2ff2e-143">Return value</span></span>

<span data-ttu-id="2ff2e-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ff2e-144">S_OK</span></span> 
  
> <span data-ttu-id="2ff2e-145">Le dossier a été correctement copié ou déplacé.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="2ff2e-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="2ff2e-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="2ff2e-147">Le nom du dossier déplacé ou copié est le même que celui d'un sous-dossier dans le dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="2ff2e-148">Le fournisseur de banque de messages exige que les noms de dossier soient uniques.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="2ff2e-149">L'opération s'arrête sans terminer.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="2ff2e-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="2ff2e-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="2ff2e-151">L'appel a réussi, mais toutes les entrées n'ont pas été correctement copiées.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="2ff2e-152">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="2ff2e-153">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="2ff2e-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2ff2e-154">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="2ff2e-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ff2e-155">Remarques</span><span class="sxs-lookup"><span data-stu-id="2ff2e-155">Remarks</span></span>

<span data-ttu-id="2ff2e-156">La méthode **IMAPISupport:: CopyFolder** est implémentée pour les objets de prise en charge du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="2ff2e-157">Les fournisseurs de banques de messages peuvent appeler **IMAPISupport: CopyFolder** dans leur implémentation de [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) pour copier ou déplacer un dossier unique d'un dossier parent vers un autre.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="2ff2e-158">**IMAPISupport:: CopyFolder** ajoute le dossier copié ou déplacé en tant que sous-dossier du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2ff2e-159">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="2ff2e-159">Notes to callers</span></span>

 <span data-ttu-id="2ff2e-160">**IMAPISupport:: CopyFolder** permet le changement de nom et le transfert simultanés de dossiers, ainsi que la copie ou le transfert des sous-dossiers du dossier affecté.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="2ff2e-161">Pour copier ou déplacer tous les sous-dossiers imbriqués dans le dossier copié ou déplacé, transmettez l'indicateur COPY_SUBFOLDERS dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="2ff2e-162">Prévoyez les valeurs de retour suivantes dans les conditions suivantes:</span><span class="sxs-lookup"><span data-stu-id="2ff2e-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="2ff2e-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="2ff2e-163">**Condition**</span></span>|<span data-ttu-id="2ff2e-164">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="2ff2e-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2ff2e-165">**CopyFolder** a copié ou déplacé le dossier et tous ses sous-dossiers, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="2ff2e-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ff2e-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="2ff2e-167">**CopyFolder** n'a pas pu copier ou déplacer tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="2ff2e-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="2ff2e-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="2ff2e-169">**CopyFolder** n'a pas pu être terminé.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="2ff2e-170">Toute valeur d'erreur</span><span class="sxs-lookup"><span data-stu-id="2ff2e-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="2ff2e-171">Si **CopyFolder** renvoie une valeur d'erreur, ne continuez pas en supposant qu'aucun travail n'a été effectué.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="2ff2e-172">Un ou plusieurs dossiers ont pu être copiés ou déplacés avant que **CopyFolder** ait rencontré l'échec.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ff2e-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ff2e-173">See also</span></span>



[<span data-ttu-id="2ff2e-174">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ff2e-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

