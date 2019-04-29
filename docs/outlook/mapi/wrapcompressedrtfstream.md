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
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439799"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="4043a-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="4043a-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="4043a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4043a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4043a-105">Crée un flux de texte au format RTF non compressé à partir du format compressé utilisé dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4043a-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4043a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4043a-106">Header file:</span></span>  <br/> |<span data-ttu-id="4043a-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4043a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4043a-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="4043a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4043a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4043a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4043a-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="4043a-110">Called by:</span></span>  <br/> |<span data-ttu-id="4043a-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="4043a-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="4043a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4043a-112">Parameters</span></span>

 <span data-ttu-id="4043a-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="4043a-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="4043a-114">dans Pointeur vers un flux ouvert sur la propriété PR_RTF_COMPRESSED d'un message.</span><span class="sxs-lookup"><span data-stu-id="4043a-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="4043a-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4043a-115">_ulFlags_</span></span>
  
> <span data-ttu-id="4043a-116">dans Masque de masque des indicateurs d'option pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="4043a-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="4043a-117">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="4043a-117">The following flags can be set:</span></span>
    
<span data-ttu-id="4043a-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4043a-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="4043a-119">Indique si le client envisage de lire ou d'écrire l'interface de flux encapsulé qui est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="4043a-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="4043a-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="4043a-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="4043a-121">Le format RTF non compressé doit être écrit dans le flux vers lequel pointe _lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="4043a-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="4043a-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="4043a-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="4043a-123">remarquer Pointeur vers l'emplacement où **WrapCompressedRTFStream** renvoie un flux pour le format RTF non compressé.</span><span class="sxs-lookup"><span data-stu-id="4043a-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4043a-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4043a-124">Return value</span></span>

<span data-ttu-id="4043a-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="4043a-125">S_OK</span></span> 
  
> <span data-ttu-id="4043a-126">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4043a-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4043a-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="4043a-127">Remarks</span></span>

<span data-ttu-id="4043a-128">Si l'indicateur MAPI_MODIFY est transmis dans le paramètre _ulFlags_ , le paramètre _lpCompressedRTFStream_ doit déjà être ouvert en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="4043a-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="4043a-129">Le nouveau texte RTF non compressé doit être écrit dans l'interface de flux renvoyée dans _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="4043a-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="4043a-130">Étant donné qu'il n'est pas possible d'ajouter le flux existant, le texte du message entier doit être écrit.</span><span class="sxs-lookup"><span data-stu-id="4043a-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="4043a-131">Si la valeur de zéro est transmise au paramètre _ulFlags_ , _lpCompressedRTFStream_ peut être ouvert en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4043a-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="4043a-132">Seul le texte du message entier peut être lu à partir de l'interface de flux renvoyée dans _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="4043a-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="4043a-133">Il n'est pas possible d'effectuer une recherche à partir du milieu du flux.</span><span class="sxs-lookup"><span data-stu-id="4043a-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="4043a-134">**WrapCompressedRTFStream** part du principe que le pointeur du flux compressé est défini au début du flux.</span><span class="sxs-lookup"><span data-stu-id="4043a-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="4043a-135">Certaines méthodes OLE **IStream** ne sont pas prises en charge par le flux non compressé renvoyé.</span><span class="sxs-lookup"><span data-stu-id="4043a-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="4043a-136">Il s'agit notamment de **IStream:: Clone**, **IStream:: LockRegion**, **IStream:: Revert**, **IStream:: Seek**, **IStream:: assets**, **IStream:: stat**et **IStream:: UnlockRegion**.</span><span class="sxs-lookup"><span data-stu-id="4043a-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="4043a-137">Pour copier dans le flux entier, une boucle en lecture/écriture est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4043a-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="4043a-138">Étant donné que le client écrit le nouveau format RTF sous une forme non compressée, il doit utiliser **WrapCompressedRTFStream**, au lieu d'écrire directement dans le flux.</span><span class="sxs-lookup"><span data-stu-id="4043a-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="4043a-139">Les clients prenant en charge le format RTF doivent Rechercher l'indicateur STORE_UNCOMPRESSED_RTF dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) et le transmettre à **WrapCompressed RTFStream** s'il est défini.</span><span class="sxs-lookup"><span data-stu-id="4043a-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4043a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4043a-140">See also</span></span>



[<span data-ttu-id="4043a-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="4043a-141">RTFSync</span></span>](rtfsync.md)

