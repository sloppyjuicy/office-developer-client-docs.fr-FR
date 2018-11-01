---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a7095907a1fb437e225922d0bef08b4ad79a4b6f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594592"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="f8332-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="f8332-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="f8332-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8332-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8332-105">Crée un flux de texte dans décompressé texte enrichi (RTF) au format compressé utilisée dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f8332-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8332-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f8332-106">Header file:</span></span>  <br/> |<span data-ttu-id="f8332-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8332-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f8332-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f8332-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f8332-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f8332-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f8332-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f8332-110">Called by:</span></span>  <br/> |<span data-ttu-id="f8332-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="f8332-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="f8332-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8332-112">Parameters</span></span>

 <span data-ttu-id="f8332-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f8332-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="f8332-114">[in] Pointeur vers un objet stream ouvert sur la propriété PR_RTF_COMPRESSED d’un message.</span><span class="sxs-lookup"><span data-stu-id="f8332-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="f8332-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8332-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f8332-116">[in] Masque de bits d’indicateurs d’option de la fonction.</span><span class="sxs-lookup"><span data-stu-id="f8332-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="f8332-117">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="f8332-117">The following flags can be set:</span></span>
    
<span data-ttu-id="f8332-118">N'</span><span class="sxs-lookup"><span data-stu-id="f8332-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f8332-119">Si le client a l’intention de lire ou écrire l’interface de flux encapsulé est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f8332-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="f8332-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="f8332-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="f8332-121">RTF décompressé doit être écrits dans le flux vers lequel pointé _lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f8332-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="f8332-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f8332-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="f8332-123">[out] Pointeur vers l’emplacement où **WrapCompressedRTFStream** renvoie un flux de données pour le format RTF décompressé.</span><span class="sxs-lookup"><span data-stu-id="f8332-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f8332-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f8332-124">Return value</span></span>

<span data-ttu-id="f8332-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8332-125">S_OK</span></span> 
  
> <span data-ttu-id="f8332-126">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f8332-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8332-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="f8332-127">Remarks</span></span>

<span data-ttu-id="f8332-128">Si l’indicateur n’est passé dans le paramètre _ulFlags_ , le paramètre _lpCompressedRTFStream_ doit déjà être ouvert pour la lecture et écriture.</span><span class="sxs-lookup"><span data-stu-id="f8332-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="f8332-129">Nouveau texte RTF décompressé doit être écrits dans l’interface de flux de données retournée dans _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="f8332-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="f8332-130">Car il n’est pas possible d’ajouter le flux existant, le texte de l’intégralité du message doit être écrite.</span><span class="sxs-lookup"><span data-stu-id="f8332-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="f8332-131">Si la valeur zéro est transmise dans le paramètre _ulFlags_ , _lpCompressedRTFStream_ peut être ouvert en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f8332-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="f8332-132">Seul le texte de l’intégralité du message peut être lue en dehors de l’interface de flux de données retournée dans _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="f8332-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="f8332-133">Il n’est pas possible de rechercher le démarrage du milieu de l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="f8332-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="f8332-134">**WrapCompressedRTFStream** suppose que le pointeur du flux compressé est définie au début de l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="f8332-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="f8332-135">Certaines méthodes OLE **IStream** ne sont pas pris en charge par le flux non compressé retourné.</span><span class="sxs-lookup"><span data-stu-id="f8332-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="f8332-136">Cela inclut les **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**et **IStream::UnlockRegion**.</span><span class="sxs-lookup"><span data-stu-id="f8332-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="f8332-137">Pour pouvoir la copier sur l’intégralité du flux, une boucle de lecture/écriture est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f8332-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="f8332-138">Étant donné que le client écrit nouveau RTF au format non compressé, elle doit utiliser **WrapCompressedRTFStream**, au lieu d’écrire directement dans le flux.</span><span class="sxs-lookup"><span data-stu-id="f8332-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="f8332-139">Clients prenant en charge les RTF doivent rechercher l’indicateur STORE_UNCOMPRESSED_RTF dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) et passez-le à **WrapCompressed RTFStream** si elle est définie.</span><span class="sxs-lookup"><span data-stu-id="f8332-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f8332-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8332-140">See also</span></span>



[<span data-ttu-id="f8332-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="f8332-141">RTFSync</span></span>](rtfsync.md)

