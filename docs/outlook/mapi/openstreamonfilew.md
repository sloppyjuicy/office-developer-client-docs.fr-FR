---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406023"
---
# <a name="openstreamonfilew"></a><span data-ttu-id="e30cc-103">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="e30cc-103">OpenStreamOnFileW</span></span>

  
  
<span data-ttu-id="e30cc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e30cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e30cc-105">Alloue et initialise un objet OLE **IStream** pour accéder au contenu d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="e30cc-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="e30cc-106">Cette fonction prend les chaînes UNICODE en tant qu’arguments, contrairement à la version ANSI de cette fonction [OpenStreamOnFile](openstreamonfile.md), et autorise donc les caractères arbitraires dans le nom de fichier, y compris le chemin d’accès et l’extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="e30cc-106">This function takes UNICODE strings as arguments, unlike the ANSI version of this function [OpenStreamOnFile](openstreamonfile.md), and thus allows for arbitrary characters in the file name including the path and file extension.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e30cc-107">Exporté par :</span><span class="sxs-lookup"><span data-stu-id="e30cc-107">Exported by:</span></span>  <br/> |<span data-ttu-id="e30cc-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="e30cc-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="e30cc-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e30cc-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="e30cc-110">Outlook</span><span class="sxs-lookup"><span data-stu-id="e30cc-110">Outlook</span></span>  <br/> |
|<span data-ttu-id="e30cc-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e30cc-111">Called by:</span></span>  <br/> |<span data-ttu-id="e30cc-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e30cc-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="e30cc-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="e30cc-113">Parameters</span></span>

 <span data-ttu-id="e30cc-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e30cc-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e30cc-115">[in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e30cc-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="e30cc-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e30cc-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e30cc-117">[in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e30cc-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="e30cc-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e30cc-118">_ulFlags_</span></span>
  
> <span data-ttu-id="e30cc-119">[in] Masque de bits d’indicateurs utilisés pour contrôler la création ou l’ouverture du fichier à accéder via l’objet OLE **IStream.**</span><span class="sxs-lookup"><span data-stu-id="e30cc-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="e30cc-120">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="e30cc-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="e30cc-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="e30cc-121">SOF_UNIQUEFILENAME</span></span>
  
> <span data-ttu-id="e30cc-122">Un fichier temporaire doit être créé pour **l’objet IStream.**</span><span class="sxs-lookup"><span data-stu-id="e30cc-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="e30cc-123">Si cet indicateur est définie, les STGM_CREATE et STGM_READWRITE doivent également être définies.</span><span class="sxs-lookup"><span data-stu-id="e30cc-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="e30cc-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="e30cc-124">STGM_CREATE</span></span>
  
> <span data-ttu-id="e30cc-125">Le fichier doit être créé même s’il en existe déjà un.</span><span class="sxs-lookup"><span data-stu-id="e30cc-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="e30cc-126">Si le  _paramètre lpszFileName_ n’est pas paramétré, cet indicateur et STGM_DELETEONRELEASE doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="e30cc-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="e30cc-127">Si STGM_CREATE est définie, l’STGM_READWRITE doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="e30cc-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="e30cc-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="e30cc-128">STGM_DELETEONRELEASE</span></span>
  
> <span data-ttu-id="e30cc-129">Le fichier doit être supprimé lorsque **l’objet IStream** est libéré.</span><span class="sxs-lookup"><span data-stu-id="e30cc-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="e30cc-130">Si le  _paramètre lpszFileName_ n’est pas paramétré, cet indicateur et STGM_CREATE doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="e30cc-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="e30cc-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="e30cc-131">STGM_READ</span></span>
  
> <span data-ttu-id="e30cc-132">Le fichier doit être créé ou ouvert avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e30cc-132">The file is to be created or opened with read-only access.</span></span>
    
<span data-ttu-id="e30cc-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="e30cc-133">STGM_READWRITE</span></span>
  
> <span data-ttu-id="e30cc-134">Le fichier doit être créé ou ouvert avec une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e30cc-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="e30cc-135">Si cet indicateur n’est pas STGM_CREATE, l’indicateur de STGM_CREATE ne doit pas l’être non plus.</span><span class="sxs-lookup"><span data-stu-id="e30cc-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span>
    
 <span data-ttu-id="e30cc-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="e30cc-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="e30cc-137">[in] Nom du fichier, y compris le chemin d’accès et l’extension, du fichier nommé Unicode pour lequel **OpenStreamOnFileW** initialise **l’objet IStream.**</span><span class="sxs-lookup"><span data-stu-id="e30cc-137">[in] The filename, including path and extension, of the Unicode named file for which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="e30cc-138">Si l SOF_UNIQUEFILENAME est définie,  _lpszFileName_ contient le chemin d’accès au répertoire dans lequel créer un fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="e30cc-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="e30cc-139">Si  _lpszFileName_ est NULL, **OpenStreamOnFileW** obtient un chemin d’accès approprié à partir du système et les indicateurs STGM_CREATE et STGM_DELETEONRELEASE doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="e30cc-139">If  _lpszFileName_ is NULL, **OpenStreamOnFileW** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="e30cc-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="e30cc-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="e30cc-141">[in] Préfixe du nom de fichier Unicode sur lequel **OpenStreamOnFileW** initialise **l’objet IStream.**</span><span class="sxs-lookup"><span data-stu-id="e30cc-141">[in] The prefix for the Unicode filename on which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="e30cc-142">S’il est définie, le préfixe ne doit pas contenir plus de trois caractères.</span><span class="sxs-lookup"><span data-stu-id="e30cc-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="e30cc-143">Si  _lpszPrefix_ a la valeur NULL, un préfixe « SOF » est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e30cc-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="e30cc-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="e30cc-144">_lppStream_</span></span>
  
> <span data-ttu-id="e30cc-145">[out] Pointeur vers un pointeur vers un objet exposant l’interface **IStream.**</span><span class="sxs-lookup"><span data-stu-id="e30cc-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e30cc-146">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e30cc-146">Return value</span></span>

<span data-ttu-id="e30cc-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="e30cc-147">S_OK</span></span>
  
> <span data-ttu-id="e30cc-148">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e30cc-148">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e30cc-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e30cc-149">MAPI_E_NO_ACCESS</span></span>
  
> <span data-ttu-id="e30cc-150">Le fichier n’a pas pu être accessible en raison d’autorisations utilisateur insuffisantes ou parce que les fichiers en lecture seule ne peuvent pas être modifiés.</span><span class="sxs-lookup"><span data-stu-id="e30cc-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span>
    
<span data-ttu-id="e30cc-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e30cc-151">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="e30cc-152">Le fichier désigné n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="e30cc-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e30cc-153">Remarques</span><span class="sxs-lookup"><span data-stu-id="e30cc-153">Remarks</span></span>

<span data-ttu-id="e30cc-154">La **fonction OpenStreamOnFileW** a deux utilisations importantes en plus de la gestion d’un fichier avec un nom Unicode, qui se distingue par le paramètre de l’indicateur SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="e30cc-154">The **OpenStreamOnFileW** function has two important uses in addition to handling a file with a Unicode name, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="e30cc-155">Lorsque cet indicateur n’est pas définie, **OpenStreamOnFileW** ouvre un objet **IStream** sur un fichier existant, par exemple pour copier son contenu dans la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) d’une pièce jointe à l’aide de la méthode **IStream::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="e30cc-155">When this flag is not set, **OpenStreamOnFileW** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="e30cc-156">Dans ce cas,  _le paramètre lpszFileName_ spécifie le chemin d’accès et le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="e30cc-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="e30cc-157">Lorsque SOF_UNIQUEFILENAME est définie, **OpenStreamOnFileW** crée un fichier temporaire pour contenir les données **d’un objet IStream.**</span><span class="sxs-lookup"><span data-stu-id="e30cc-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFileW** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="e30cc-158">Pour cette utilisation, le paramètre  _lpszFileName_ peut éventuellement désigner le chemin d’accès au répertoire dans lequel le fichier doit être créé, et le paramètre  _lpszPrefix_ peut éventuellement spécifier un préfixe pour le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="e30cc-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="e30cc-159">Lorsque l’application cliente ou le fournisseur de services appelant a terminé avec l’objet **IStream,** il doit le libérer en appelant la méthode OLE **IStream::Release.**</span><span class="sxs-lookup"><span data-stu-id="e30cc-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="e30cc-160">MAPI utilise les fonctions pointées par  _lpAllocateBuffer_ et  _lpFreeBuffer_ pour la plupart de l’allocation et de la déallocation de la mémoire, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel d’interfaces objet telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="e30cc-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e30cc-161">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="e30cc-161">Notes to callers</span></span>

<span data-ttu-id="e30cc-162">L SOF_UNIQUEFILENAME est utilisé pour créer un fichier temporaire avec un nom propre au système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e30cc-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="e30cc-163">Si cet indicateur est définie, le paramètre  _lpszFileName_ specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span><span class="sxs-lookup"><span data-stu-id="e30cc-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="e30cc-164">Le nom de fichier construit est <prefix> HHHH. TMP, où HHHH est un nombre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="e30cc-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="e30cc-165">Si _lpszFileName_ est NULL, le fichier est créé dans le répertoire de fichiers temporaire qui est renvoyé à partir de la fonction Windows **GetTempPath** ou le répertoire actuel si aucun répertoire de fichiers temporaire n’a été désigné.</span><span class="sxs-lookup"><span data-stu-id="e30cc-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span>
  
<span data-ttu-id="e30cc-166">Si l’indicateur SOF_UNIQUEFILENAME n’est pas définie,  _lpszPrefix_ est ignoré et  _lpszFileName_ doit contenir le chemin d’accès complet et le nom du fichier à ouvrir ou à créer.</span><span class="sxs-lookup"><span data-stu-id="e30cc-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="e30cc-167">Le fichier sera ouvert ou créé en fonction des autres indicateurs qui sont définies dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e30cc-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e30cc-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e30cc-168">See also</span></span>



[<span data-ttu-id="e30cc-169">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="e30cc-169">OpenStreamOnFile</span></span>](openstreamonfile.md)

