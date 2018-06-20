---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8c246968dcac719a8ee8177e20e802f9c7033435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784947"
---
# <a name="openstreamonfile"></a><span data-ttu-id="661b1-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="661b1-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="661b1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="661b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="661b1-105">Alloue et initialise un objet OLE **IStream** pour accéder au contenu d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="661b1-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="661b1-106">Cette fonction accepte une chaîne ANSI comme le nom de fichier, y compris le chemin d’accès et l’extension de fichier, par conséquent, l’utilisation de la version Unicode de cette fonction, [OpenStreamOnFileW](openstreamonfilew.md), est recommandé.</span><span class="sxs-lookup"><span data-stu-id="661b1-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="661b1-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="661b1-107">Header file:</span></span>  <br/> |<span data-ttu-id="661b1-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="661b1-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="661b1-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="661b1-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="661b1-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="661b1-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="661b1-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="661b1-111">Called by:</span></span>  <br/> |<span data-ttu-id="661b1-112">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="661b1-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="661b1-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="661b1-113">Parameters</span></span>

 <span data-ttu-id="661b1-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="661b1-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="661b1-115">[in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="661b1-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="661b1-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="661b1-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="661b1-117">[in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="661b1-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="661b1-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="661b1-118">_ulFlags_</span></span>
  
> <span data-ttu-id="661b1-119">[in] Masque de bits d’indicateurs utilisés pour contrôler la création ou l’ouverture du fichier à accessible par le biais de l’objet OLE **IStream** .</span><span class="sxs-lookup"><span data-stu-id="661b1-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="661b1-120">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="661b1-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="661b1-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="661b1-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="661b1-122">Un fichier temporaire doit être créé pour l’objet **IStream** .</span><span class="sxs-lookup"><span data-stu-id="661b1-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="661b1-123">Si cet indicateur est défini, les indicateurs STGM_CREATE et STGM_READWRITE doivent également être définies.</span><span class="sxs-lookup"><span data-stu-id="661b1-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="661b1-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="661b1-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="661b1-125">Le fichier doit être créé même si elle existe déjà.</span><span class="sxs-lookup"><span data-stu-id="661b1-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="661b1-126">Si le paramètre _lpszFileName_ n’est pas défini, cet indicateur et la STGM_DELETEONRELEASE doivent être définie.</span><span class="sxs-lookup"><span data-stu-id="661b1-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="661b1-127">Si STGM_CREATE est défini, l’indicateur STGM_READWRITE doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="661b1-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="661b1-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="661b1-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="661b1-129">Le fichier doit être supprimé lors de l’objet **IStream** .</span><span class="sxs-lookup"><span data-stu-id="661b1-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="661b1-130">Si le paramètre _lpszFileName_ n’est pas défini, cet indicateur et la STGM_CREATE doivent être définie.</span><span class="sxs-lookup"><span data-stu-id="661b1-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="661b1-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="661b1-131">STGM_READ</span></span> 
  
> <span data-ttu-id="661b1-132">Le fichier doit être créé ou ouvert avec accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="661b1-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="661b1-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="661b1-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="661b1-134">Le fichier doit être créé ou ouvert avec l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="661b1-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="661b1-135">Si cet indicateur n’est pas défini, l’indicateur STGM_CREATE ne doit pas être définie soit.</span><span class="sxs-lookup"><span data-stu-id="661b1-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="661b1-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="661b1-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="661b1-137">[in] Nom de fichier, y compris le chemin d’accès et l’extension du fichier pour lequel **OpenStreamOnFile** initialise l’objet **IStream** .</span><span class="sxs-lookup"><span data-stu-id="661b1-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="661b1-138">Si l’indicateur SOF_UNIQUEFILENAME est défini, _lpszFileName_ contient le chemin d’accès au répertoire dans lequel vous souhaitez créer un fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="661b1-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="661b1-139">Si _lpszFileName_ est NULL, **OpenStreamOnFile** Obtient un chemin d’accès approprié à partir du système et indicateurs STGM_DELETEONRELEASE et STGM_CREATE doivent être définis.</span><span class="sxs-lookup"><span data-stu-id="661b1-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="661b1-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="661b1-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="661b1-141">[in] Préfixe de nom de fichier sur lequel **OpenStreamOnFile** initialise l’objet **IStream** .</span><span class="sxs-lookup"><span data-stu-id="661b1-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="661b1-142">Si défini, le préfixe doit contenir pas plus de trois caractères.</span><span class="sxs-lookup"><span data-stu-id="661b1-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="661b1-143">Si _lpszPrefix_ est NULL, le préfixe « SOF » est utilisé.</span><span class="sxs-lookup"><span data-stu-id="661b1-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="661b1-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="661b1-144">_lppStream_</span></span>
  
> <span data-ttu-id="661b1-145">[out] Pointeur vers un pointeur vers un objet exposition de l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="661b1-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="661b1-146">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="661b1-146">Return value</span></span>

<span data-ttu-id="661b1-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="661b1-147">S_OK</span></span> 
  
> <span data-ttu-id="661b1-148">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="661b1-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="661b1-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="661b1-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="661b1-150">Le fichier est inaccessible en raison d’autorisations insuffisantes utilisateur ou parce que les fichiers en lecture seule ne peut pas être modifiés.</span><span class="sxs-lookup"><span data-stu-id="661b1-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="661b1-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="661b1-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="661b1-152">Le fichier désigné n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="661b1-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="661b1-153">Remarques</span><span class="sxs-lookup"><span data-stu-id="661b1-153">Remarks</span></span>

<span data-ttu-id="661b1-154">La fonction **OpenStreamOnFile** a deux utilisations importantes, caractérisées par le paramètre de l’indicateur SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="661b1-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="661b1-155">Lorsque cet indicateur n’est pas défini, **OpenStreamOnFile** ouvre un objet **IStream** sur un fichier existant, par exemple pour copier son contenu dans la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) d’une pièce jointe à l’aide de la **IStream :: CopyTo** méthode.</span><span class="sxs-lookup"><span data-stu-id="661b1-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="661b1-156">Dans ce cas, le paramètre _lpszFileName_ Spécifie le chemin d’accès et le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="661b1-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="661b1-157">Lorsque SOF_UNIQUEFILENAME est défini, **OpenStreamOnFile** crée un fichier temporaire pour stocker les données d’un objet **IStream** .</span><span class="sxs-lookup"><span data-stu-id="661b1-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="661b1-158">Pour cela, le paramètre _lpszFileName_ peut désigner éventuellement le chemin d’accès au répertoire où le fichier doit être créé, et le paramètre _lpszPrefix_ peut éventuellement spécifier un préfixe pour le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="661b1-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="661b1-159">Lorsque l’application cliente appelant ou un fournisseur de services est terminé avec l’objet **IStream** , il doit le libérer en appelant la méthode OLE **IStream::Release** .</span><span class="sxs-lookup"><span data-stu-id="661b1-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="661b1-160">MAPI utilise les fonctions désignées par _lpAllocateBuffer_ et _lpFreeBuffer_ pour la plupart de l’allocation de mémoire et de désaffectation, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel des interfaces de l’objet tel que [IMAPIProp :: GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="661b1-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="661b1-161">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="661b1-161">Notes to callers</span></span>

<span data-ttu-id="661b1-162">L’indicateur SOF_UNIQUEFILENAME est utilisé pour créer un fichier temporaire avec un nom unique pour le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="661b1-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="661b1-163">Si cet indicateur est défini, la spécifie de paramètre _lpszFileName_ le chemin d’accès pour le fichier temporaire et le paramètre _lpszPrefix_ contient les premiers caractères du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="661b1-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="661b1-164">Est le nom de fichier construit <prefix>HHHH. TMP, où HHHH est un nombre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="661b1-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="661b1-165">Si _lpszFileName_ est NULL, le fichier sera créé dans le répertoire du fichier temporaire qui est renvoyé à partir de la fonction Windows **GetTempPath**ou le répertoire actif si aucun répertoire de fichiers temporaires n’a été désigné.</span><span class="sxs-lookup"><span data-stu-id="661b1-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="661b1-166">Si l’indicateur SOF_UNIQUEFILENAME n’est pas définie, _lpszPrefix_ est ignorée et _lpszFileName_ doit contenir le chemin d’accès complet et le nom du fichier à être ouvert ou créé.</span><span class="sxs-lookup"><span data-stu-id="661b1-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="661b1-167">Le fichier est ouvert ou créé selon les autres indicateurs qui sont définis dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="661b1-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="661b1-168">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="661b1-168">MFCMAPI reference</span></span>

<span data-ttu-id="661b1-169">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="661b1-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="661b1-170">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="661b1-170">**File**</span></span>|<span data-ttu-id="661b1-171">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="661b1-171">**Function**</span></span>|<span data-ttu-id="661b1-172">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="661b1-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="661b1-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="661b1-173">File.cpp</span></span>  <br/> |<span data-ttu-id="661b1-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="661b1-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="661b1-175">MFCMAPI utilise la méthode **OpenStreamOnFile** pour ouvrir un objet stream dans un fichier peut être écrites une pièce jointe à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="661b1-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="661b1-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="661b1-176">See also</span></span>



[<span data-ttu-id="661b1-177">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="661b1-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

