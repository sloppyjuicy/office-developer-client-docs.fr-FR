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
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="0e050-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="0e050-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="0e050-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e050-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e050-105">Crée un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="0e050-105">Creates a new subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0e050-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e050-106">Parameters</span></span>

 <span data-ttu-id="0e050-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="0e050-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="0e050-108">dans Type de dossier à créer.</span><span class="sxs-lookup"><span data-stu-id="0e050-108">[in] The type of folder to create.</span></span> <span data-ttu-id="0e050-109">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="0e050-109">The following flags can be set:</span></span>
    
<span data-ttu-id="0e050-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="0e050-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="0e050-111">Un dossier générique doit être créé.</span><span class="sxs-lookup"><span data-stu-id="0e050-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="0e050-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="0e050-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="0e050-113">Un dossier de résultats de recherche doit être créé.</span><span class="sxs-lookup"><span data-stu-id="0e050-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="0e050-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="0e050-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="0e050-115">dans Pointeur vers une chaîne qui contient le nom du nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="0e050-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="0e050-116">Ce nom est la base de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="0e050-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="0e050-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="0e050-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="0e050-118">dans Pointeur vers une chaîne qui contient un commentaire associé au nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="0e050-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="0e050-119">Cette chaîne devient la valeur de la propriété **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) du nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="0e050-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="0e050-120">Si la valeur NULL est transmise, le dossier n'a pas de commentaire initial.</span><span class="sxs-lookup"><span data-stu-id="0e050-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="0e050-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0e050-121">_lpInterface_</span></span>
  
> <span data-ttu-id="0e050-122">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="0e050-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="0e050-123">En passant NULL, le fournisseur de banque de messages renvoie l'interface de dossier standard, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0e050-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="0e050-124">Les clients doivent transmettre la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="0e050-124">Clients must pass NULL.</span></span> <span data-ttu-id="0e050-125">Les autres appelants peuvent définir le paramètre _lpInterface_ sur IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="0e050-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="0e050-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e050-126">_ulFlags_</span></span>
  
> <span data-ttu-id="0e050-127">dans Masque de des indicateurs qui contrôle la manière dont le dossier est créé.</span><span class="sxs-lookup"><span data-stu-id="0e050-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="0e050-128">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="0e050-128">The following flags can be set:</span></span>
    
<span data-ttu-id="0e050-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0e050-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0e050-130">Permet le renvoi correct de **CreateFolder** , éventuellement avant que le nouveau dossier soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="0e050-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="0e050-131">Si le nouveau dossier n'est pas disponible, une erreur peut se produire lors d'un appel ultérieur.</span><span class="sxs-lookup"><span data-stu-id="0e050-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="0e050-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0e050-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0e050-133">Le nom du dossier est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e050-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="0e050-134">Si l'indicateur MAPI_UNICODE n'est pas défini, le nom du dossier est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="0e050-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="0e050-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="0e050-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="0e050-136">Autorise la méthode à aboutir même si le dossier nommé dans le paramètre _lpszFolderName_ existe déjà en ouvrant le dossier existant qui porte ce nom.</span><span class="sxs-lookup"><span data-stu-id="0e050-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="0e050-137">Notez que les fournisseurs de banques de messages qui permettent aux dossiers frères de posséder le même nom peuvent ne pas ouvrir un dossier existant s'il en existe plusieurs avec le nom fourni.</span><span class="sxs-lookup"><span data-stu-id="0e050-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="0e050-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="0e050-138">_lppFolder_</span></span>
  
> <span data-ttu-id="0e050-139">remarquer Pointeur vers un pointeur vers le dossier nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="0e050-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e050-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0e050-140">Return value</span></span>

<span data-ttu-id="0e050-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e050-141">S_OK</span></span> 
  
> <span data-ttu-id="0e050-142">Le nouveau dossier a été créé ou ouvert avec succès, si l'indicateur OPEN_IF_EXISTS est défini.</span><span class="sxs-lookup"><span data-stu-id="0e050-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="0e050-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0e050-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0e050-144">L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e050-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="0e050-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="0e050-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="0e050-146">Un dossier dont le nom est indiqué dans le paramètre _lpszFolderName_ existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0e050-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="0e050-147">Les noms de dossier doivent être uniques.</span><span class="sxs-lookup"><span data-stu-id="0e050-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e050-148">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e050-148">Remarks</span></span>

<span data-ttu-id="0e050-149">La méthode **IMAPIFolder:: CreateFolder** crée un sous-dossier dans le dossier actif et affecte un identificateur d'entrée au nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="0e050-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0e050-150">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="0e050-150">Notes to callers</span></span>

<span data-ttu-id="0e050-151">Lorsque **CreateFolder** renvoie, Notez que l'identificateur d'entrée pour le nouveau dossier peut ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="0e050-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="0e050-152">Certains fournisseurs de banques de messages ne rendent pas d'identificateurs d'entrée disponibles tant que vous n'avez pas appelé la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du nouveau dossier pour l'enregistrer définitivement.</span><span class="sxs-lookup"><span data-stu-id="0e050-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="0e050-153">Cela est particulièrement vrai si vous avez défini l'indicateur MAPI_DEFERRED_ERRORS.</span><span class="sxs-lookup"><span data-stu-id="0e050-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="0e050-154">N'oubliez pas que certains fournisseurs de banques de messages pointent toujours le paramètre _lppFolder_ vers l'interface standard du dossier, quelle que soit la valeur que vous transmettez pour le paramètre _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="0e050-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="0e050-155">Étant donné que le pointeur d'interface renvoyé n'est peut-être pas du type prévu, appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) du nouveau dossier pour extraire la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0e050-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="0e050-156">Si nécessaire, effectuez un cast du pointeur vers un type plus approprié avant d'effectuer d'autres appels.</span><span class="sxs-lookup"><span data-stu-id="0e050-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="0e050-157">La plupart des fournisseurs de banques de messages exigent que le nom du nouveau dossier soit unique par rapport aux noms de ses dossiers frères.</span><span class="sxs-lookup"><span data-stu-id="0e050-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="0e050-158">Pouvoir gérer la valeur d'erreur MAPI_E_COLLISION, qui est renvoyée si cette règle n'est pas suivie.</span><span class="sxs-lookup"><span data-stu-id="0e050-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="0e050-159">Pour déterminer l'identificateur d'entrée du dossier nouvellement créé, appelez la méthode **IMAPIProp:: GetProps** du nouveau dossier pour extraire sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0e050-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e050-160">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0e050-160">MFCMAPI reference</span></span>

<span data-ttu-id="0e050-161">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0e050-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e050-162">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="0e050-162">**File**</span></span>|<span data-ttu-id="0e050-163">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="0e050-163">**Function**</span></span>|<span data-ttu-id="0e050-164">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="0e050-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e050-165">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="0e050-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="0e050-166">CMsgStoreDlg:: OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="0e050-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="0e050-167">MFCMAPI utilise la méthode **CMsgStoreDlg:: OnCreateSubFolder** pour créer des dossiers dans MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="0e050-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e050-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e050-168">See also</span></span>



[<span data-ttu-id="0e050-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="0e050-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="0e050-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0e050-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="0e050-171">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="0e050-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

