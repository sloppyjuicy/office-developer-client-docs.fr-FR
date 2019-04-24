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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280177"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="fa4d0-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="fa4d0-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="fa4d0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa4d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa4d0-105">Copie ou déplace un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-105">Copies or moves a subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="fa4d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa4d0-106">Parameters</span></span>

 <span data-ttu-id="fa4d0-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="fa4d0-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="fa4d0-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fa4d0-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="fa4d0-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="fa4d0-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="fa4d0-110">dans Pointeur vers l'identificateur d'entrée du sous-dossier à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="fa4d0-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fa4d0-111">_lpInterface_</span></span>
  
> <span data-ttu-id="fa4d0-112">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au dossier vers lequel pointe le paramètre _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="fa4d0-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="fa4d0-113">Si vous passez la valeur NULL, le fournisseur de services renvoie l'interface de dossier standard, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="fa4d0-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="fa4d0-114">Les valeurs valides pour _lpInterface_ sont IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="fa4d0-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="fa4d0-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="fa4d0-116">dans Pointeur vers le dossier ouvert qui reçoit le sous-dossier copié ou déplacé.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="fa4d0-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="fa4d0-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="fa4d0-118">dans Pointeur vers le nom du dossier copié ou déplacé dans sa nouvelle destination.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="fa4d0-119">Si _lpszNewFolderName_ est défini sur null, le nom du sous-dossier source est utilisé pour le nom du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="fa4d0-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fa4d0-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="fa4d0-121">dans Handle de la fenêtre parent de l'indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="fa4d0-122">Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur FOLDER_DIALOG dans le paramètre _ulFlags_ est défini.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="fa4d0-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="fa4d0-123">_lpProgress_</span></span>
  
> <span data-ttu-id="fa4d0-124">dans Pointeur vers un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="fa4d0-125">Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="fa4d0-126">Le paramètre _lpProgress_ est ignoré sauf si l'indicateur FOLDER_DIALOG est défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="fa4d0-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa4d0-127">_ulFlags_</span></span>
  
> <span data-ttu-id="fa4d0-128">dans Masque de des indicateurs qui contrôle l'opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="fa4d0-129">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="fa4d0-129">The following flags can be set:</span></span>
    
<span data-ttu-id="fa4d0-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="fa4d0-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="fa4d0-131">Tous les sous-dossiers du sous-dossier à copier doivent également être copiés.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="fa4d0-132">Lorsque COPY_SUBFOLDERS n'est pas défini pour une opération de copie, seul le sous-dossier identifié par _lpEntryID_ est copié.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="fa4d0-133">Avec une opération de déplacement, le comportement COPY_SUBFOLDERS est la valeur par défaut, que l'indicateur soit défini ou non.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="fa4d0-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="fa4d0-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="fa4d0-135">Demande l'affichage d'un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="fa4d0-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="fa4d0-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="fa4d0-137">Le sous-dossier doit être déplacé au lieu d'être copié.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="fa4d0-138">Si FOLDER_MOVE n'est pas défini, le sous-dossier est copié.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="fa4d0-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="fa4d0-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="fa4d0-140">Informe le fournisseur de banque de messages que s'il implémente **CopyFolder** en appelant la méthode IMAPISupport de l'objet de prise en charge [::D ocopyto](imapisupport-docopyto.md) ou [IMAPISupport::D méthode ocopyprops](imapisupport-docopyprops.md) , **CopyFolder** doit renvoyer immédiatement MAPI_E_ DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="fa4d0-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fa4d0-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fa4d0-142">Le nom du dossier de destination est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="fa4d0-143">Si l'indicateur MAPI_UNICODE n'est pas défini, le nom du dossier est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa4d0-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fa4d0-144">Return value</span></span>

<span data-ttu-id="fa4d0-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa4d0-145">S_OK</span></span> 
  
> <span data-ttu-id="fa4d0-146">Le dossier spécifié a été correctement copié ou déplacé.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="fa4d0-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="fa4d0-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="fa4d0-148">L'indicateur MAPI_UNICODE a été défini et le fournisseur de banque de messages ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et le fournisseur de banque de messages prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="fa4d0-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="fa4d0-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="fa4d0-150">Le nom du dossier déplacé ou copié est le même que celui d'un sous-dossier dans le dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="fa4d0-151">Le fournisseur de banque de messages requiert des noms de dossier uniques.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="fa4d0-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="fa4d0-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="fa4d0-153">Le fournisseur implémente cette méthode en appelant une méthode d'objet de prise en charge, et l'appelant a passé l'indicateur MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="fa4d0-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="fa4d0-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="fa4d0-155">Le dossier source contient directement ou indirectement le dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="fa4d0-156">Un travail significatif a pu être effectué avant la découverte de cette condition, de sorte que le dossier source et de destination peut être partiellement modifié.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="fa4d0-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="fa4d0-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="fa4d0-158">L'appel a réussi, mais toutes les entrées n'ont pas été correctement copiées.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="fa4d0-159">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="fa4d0-160">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="fa4d0-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="fa4d0-161">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="fa4d0-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa4d0-162">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa4d0-162">Remarks</span></span>

<span data-ttu-id="fa4d0-163">La méthode **IMAPIFolder:: CopyFolder** copie ou déplace un sous-dossier d'un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="fa4d0-164">Le sous-dossier copié ou déplacé est ajouté au dossier de destination sous la forme d'un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fa4d0-165">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="fa4d0-165">Notes to implementers</span></span>

<span data-ttu-id="fa4d0-166">Lorsque l'opération de copie ou de déplacement implique plusieurs dossiers, comme indiqué par la définition de l'indicateur COPY_SUBFOLDERS, effectuez l'opération aussi complètement que possible pour chaque dossier.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="fa4d0-167">Parfois, l'un des dossiers à déplacer ou à copier n'existe pas ou a déjà été déplacé ou copié ailleurs.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="fa4d0-168">N'arrêtez pas l'opération prématurément à moins qu'une défaillance ne se produise au-delà de votre contrôle, telle qu'une mémoire insuffisante, un manque d'espace disque ou une corruption de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="fa4d0-169">Essayez de conserver tous les identificateurs d'entrée de message dans les messages copiés.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="fa4d0-170">Vous devez également essayer de conserver les identificateurs d'entrée, mais cela n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fa4d0-171">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="fa4d0-171">Notes to callers</span></span>

<span data-ttu-id="fa4d0-172">Attendez-vous à ces valeurs de retour dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="fa4d0-173">**Condition**</span><span class="sxs-lookup"><span data-stu-id="fa4d0-173">**Condition**</span></span>|<span data-ttu-id="fa4d0-174">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="fa4d0-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa4d0-175">**CopyFolder** a copié ou déplacé tous les messages et sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="fa4d0-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa4d0-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="fa4d0-177">**CopyFolder** n'a pas pu copier ou déplacer tous les messages et sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="fa4d0-178">MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fa4d0-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="fa4d0-179">**CopyFolder** n'a pas pu être terminé.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="fa4d0-180">Toute valeur d'erreur à l'exception de MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fa4d0-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="fa4d0-181">Lorsque **CopyFolder** ne parvient pas à se terminer, ne partez pas du principe qu'aucun travail n'a été effectué.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="fa4d0-182">**CopyFolder** a pu copier ou déplacer un ou plusieurs messages et sous-dossiers avant de rencontrer l'erreur.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="fa4d0-183">Si un identificateur d'entrée pour un dossier qui n'existe pas est transmis dans _lpEntryID_, **CopyFolder** renvoie MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l'implémentation de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="fa4d0-184">Selon le fournisseur de banque de messages, l'identificateur d'entrée du message d'origine peut ou non être conservé dans le message copié.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="fa4d0-185">Vous devez conserver les identificateurs d'entrée autant que possible, mais cela n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="fa4d0-186">Vous pouvez généralement compter sur les scénarios suivants:</span><span class="sxs-lookup"><span data-stu-id="fa4d0-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="fa4d0-187">Lorsque vous déplacez un dossier entre deux types différents de banques de messages, l'identificateur de l'entrée est garanti.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="fa4d0-188">Lorsque vous déplacez un dossier entre deux banques de messages du même type, l'identificateur de l'entrée est presque toujours modifié.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="fa4d0-189">Lorsque vous déplacez un dossier vers un autre emplacement dans le même magasin de messages, l'identificateur de l'entrée peut être modifié ou non, selon le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="fa4d0-190">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fa4d0-190">MFCMAPI reference</span></span>

<span data-ttu-id="fa4d0-191">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fa4d0-192">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="fa4d0-192">**File**</span></span>|<span data-ttu-id="fa4d0-193">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="fa4d0-193">**Function**</span></span>|<span data-ttu-id="fa4d0-194">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="fa4d0-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa4d0-195">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="fa4d0-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="fa4d0-196">CMsgStoreDlg:: OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="fa4d0-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="fa4d0-197">MFCMAPI utilise la méthode **IMAPIFolder:: CopyFolder** pour copier les dossiers d'un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="fa4d0-198">MFCMAPI mémorise le dossier source pendant l'opération de copie et effectue la copie lors de l'opération de collage.</span><span class="sxs-lookup"><span data-stu-id="fa4d0-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa4d0-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa4d0-199">See also</span></span>



[<span data-ttu-id="fa4d0-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="fa4d0-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="fa4d0-201">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="fa4d0-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

