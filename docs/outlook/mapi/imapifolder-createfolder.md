---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436761"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="463a5-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="463a5-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="463a5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="463a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="463a5-105">Crée un sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="463a5-105">Creates a new subfolder.</span></span>
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="463a5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="463a5-106">Parameters</span></span>

 <span data-ttu-id="463a5-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="463a5-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="463a5-108">[in] Type de dossier à créer.</span><span class="sxs-lookup"><span data-stu-id="463a5-108">[in] The type of folder to create.</span></span> <span data-ttu-id="463a5-109">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="463a5-109">The following flags can be set:</span></span>
    
<span data-ttu-id="463a5-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="463a5-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="463a5-111">Un dossier générique doit être créé.</span><span class="sxs-lookup"><span data-stu-id="463a5-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="463a5-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="463a5-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="463a5-113">Un dossier de résultats de recherche doit être créé.</span><span class="sxs-lookup"><span data-stu-id="463a5-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="463a5-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="463a5-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="463a5-115">[in] Pointeur vers une chaîne qui contient le nom du nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="463a5-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="463a5-116">Ce nom est la base de  la propriété PR_DISPLAY_NAME[(PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="463a5-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="463a5-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="463a5-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="463a5-118">[in] Pointeur vers une chaîne qui contient un commentaire associé au nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="463a5-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="463a5-119">Cette chaîne devient la valeur de  la propriété PR_COMMENT[(PidTagComment](pidtagcomment-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="463a5-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="463a5-120">Si la valeur NULL est passée, le dossier n’a pas de commentaire initial.</span><span class="sxs-lookup"><span data-stu-id="463a5-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="463a5-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="463a5-121">_lpInterface_</span></span>
  
> <span data-ttu-id="463a5-122">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="463a5-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="463a5-123">La transmission de null entraîne le fournisseur de magasin de messages à renvoyer l’interface de dossier standard, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="463a5-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="463a5-124">Les clients doivent transmettre la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="463a5-124">Clients must pass NULL.</span></span> <span data-ttu-id="463a5-125">D’autres appelants peuvent définir le paramètre  _lpInterface_ sur IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="463a5-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="463a5-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="463a5-126">_ulFlags_</span></span>
  
> <span data-ttu-id="463a5-127">[in] Masque de bits d’indicateurs qui contrôle la façon dont le dossier est créé.</span><span class="sxs-lookup"><span data-stu-id="463a5-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="463a5-128">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="463a5-128">The following flags can be set:</span></span>
    
<span data-ttu-id="463a5-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="463a5-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="463a5-130">Permet à **CreateFolder** de renvoyer correctement, éventuellement avant que le nouveau dossier soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="463a5-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="463a5-131">Si le nouveau dossier n’est pas disponible, un appel ultérieur à celui-ci peut provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="463a5-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="463a5-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="463a5-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="463a5-133">Le nom du dossier est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="463a5-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="463a5-134">Si l’MAPI_UNICODE n’est pas définie, le nom du dossier est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="463a5-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="463a5-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="463a5-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="463a5-136">Permet à la méthode de réussir même si le dossier nommé dans le paramètre  _lpszFolderName_ existe déjà en ouvrant le dossier existant portant ce nom.</span><span class="sxs-lookup"><span data-stu-id="463a5-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="463a5-137">Notez que les fournisseurs de magasins de messages qui autorisent les dossiers frères à avoir le même nom peuvent ne pas ouvrir un dossier existant s’il en existe plusieurs avec le nom fourni.</span><span class="sxs-lookup"><span data-stu-id="463a5-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="463a5-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="463a5-138">_lppFolder_</span></span>
  
> <span data-ttu-id="463a5-139">[out] Pointeur vers un pointeur vers le dossier nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="463a5-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="463a5-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="463a5-140">Return value</span></span>

<span data-ttu-id="463a5-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="463a5-141">S_OK</span></span> 
  
> <span data-ttu-id="463a5-142">Le nouveau dossier a été créé ou ouvert, si l’OPEN_IF_EXISTS est définie.</span><span class="sxs-lookup"><span data-stu-id="463a5-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="463a5-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="463a5-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="463a5-144">L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="463a5-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="463a5-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="463a5-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="463a5-146">Un dossier dont le nom est donné dans le  _paramètre lpszFolderName_ existe déjà.</span><span class="sxs-lookup"><span data-stu-id="463a5-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="463a5-147">Les noms de dossier doivent être uniques.</span><span class="sxs-lookup"><span data-stu-id="463a5-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="463a5-148">Remarques</span><span class="sxs-lookup"><span data-stu-id="463a5-148">Remarks</span></span>

<span data-ttu-id="463a5-149">La **méthode IMAPIFolder::CreateFolder** crée un sous-dossier dans le dossier actuel et affecte un identificateur d’entrée au nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="463a5-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="463a5-150">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="463a5-150">Notes to callers</span></span>

<span data-ttu-id="463a5-151">Lorsque **CreateFolder est** de retour, sachez que l’identificateur d’entrée pour le nouveau dossier n’est peut-être pas disponible.</span><span class="sxs-lookup"><span data-stu-id="463a5-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="463a5-152">Certains fournisseurs de magasins de messages ne rendent les identificateurs d’entrée disponibles qu’après avoir appelé la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du nouveau dossier pour l’enregistrer définitivement.</span><span class="sxs-lookup"><span data-stu-id="463a5-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="463a5-153">Cela est particulièrement vrai si vous avez MAPI_DEFERRED_ERRORS’indicateur.</span><span class="sxs-lookup"><span data-stu-id="463a5-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="463a5-154">Sachez que certains fournisseurs de magasins de messages pointent toujours le paramètre _lppFolder_ vers l’interface standard du dossier, quelle que soit la valeur que vous passez pour le paramètre _lpInterface._</span><span class="sxs-lookup"><span data-stu-id="463a5-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="463a5-155">Étant donné que le pointeur d’interface renvoyé peut ne pas être du type prévu, appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du nouveau dossier pour récupérer la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="463a5-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="463a5-156">Si nécessaire, castez le pointeur vers un type plus approprié avant d’effectuer d’autres appels.</span><span class="sxs-lookup"><span data-stu-id="463a5-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="463a5-157">La plupart des fournisseurs de magasins de messages exigent que le nom du nouveau dossier soit unique par rapport aux noms de ses dossiers frères.</span><span class="sxs-lookup"><span data-stu-id="463a5-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="463a5-158">Être en mesure de gérer la valeur MAPI_E_COLLISION’erreur, qui est renvoyée si cette règle n’est pas suivie.</span><span class="sxs-lookup"><span data-stu-id="463a5-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="463a5-159">Pour déterminer l’identificateur d’entrée du dossier nouvellement créé, appelez la méthode **IMAPIProp::GetProps** du nouveau dossier pour récupérer sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="463a5-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="463a5-160">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="463a5-160">MFCMAPI reference</span></span>

<span data-ttu-id="463a5-161">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="463a5-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="463a5-162">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="463a5-162">**File**</span></span>|<span data-ttu-id="463a5-163">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="463a5-163">**Function**</span></span>|<span data-ttu-id="463a5-164">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="463a5-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="463a5-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="463a5-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="463a5-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="463a5-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="463a5-167">MFCMAPI utilise **la méthode CMsgStoreDlg::OnCreateSubFolder** pour créer des dossiers dans MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="463a5-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="463a5-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="463a5-168">See also</span></span>



[<span data-ttu-id="463a5-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="463a5-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="463a5-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="463a5-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="463a5-171">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="463a5-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

