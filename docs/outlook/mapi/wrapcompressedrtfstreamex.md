---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391730"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="ae37a-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="ae37a-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="ae37a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae37a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae37a-105">Décompresse la le corps d’un message électronique qui est dans compressé texte enrichi (RTF), indique le format de l’objet stream décompressé, si vous le souhaitez convertit le flux décompressé dans son format natif et retourne le flux de données décompressé ou conversion en flux natif.</span><span class="sxs-lookup"><span data-stu-id="ae37a-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ae37a-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ae37a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae37a-107">Exportés par :</span><span class="sxs-lookup"><span data-stu-id="ae37a-107">Exported by:</span></span>  <br/> |<span data-ttu-id="ae37a-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="ae37a-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="ae37a-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="ae37a-109">Called by:</span></span>  <br/> |<span data-ttu-id="ae37a-110">Client</span><span class="sxs-lookup"><span data-stu-id="ae37a-110">Client</span></span>  <br/> |
|<span data-ttu-id="ae37a-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="ae37a-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ae37a-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="ae37a-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="ae37a-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae37a-113">Parameters</span></span>

<span data-ttu-id="ae37a-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="ae37a-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="ae37a-115">[in] Il s’agit d’un pointeur vers un flux qui est ouvert sur la [Propriété canonique PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) d’un message.</span><span class="sxs-lookup"><span data-stu-id="ae37a-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="ae37a-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="ae37a-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="ae37a-117">[in] Il s’agit d’un pointeur vers un</span><span class="sxs-lookup"><span data-stu-id="ae37a-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="ae37a-118">Structure [RTF_WCSINFO](rtf_wcsinfo.md) qui contient les options de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ae37a-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="ae37a-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="ae37a-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="ae37a-120">[out] Il s’agit d’un pointeur vers l’emplacement où un flux pour le format RTF décompressé est retourné.</span><span class="sxs-lookup"><span data-stu-id="ae37a-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="ae37a-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="ae37a-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="ae37a-122">[out] Il s’agit d’un pointeur vers une structure [RTF_WCSRETINFO](rtf_wcsretinfo.md) qui contient des informations sur le format du flux décompressé renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ae37a-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ae37a-123">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ae37a-123">Return values</span></span>

<span data-ttu-id="ae37a-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae37a-124">S_OK</span></span> 
  
- <span data-ttu-id="ae37a-125">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="ae37a-125">The function call is successful.</span></span>
    
<span data-ttu-id="ae37a-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ae37a-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="ae37a-127">Il est renvoyé si l’indicateur **MAPI_NATIVE_BODY** est combiné avec l’indicateur **ne** dans le champ **ulFlags** de la structure **RTF_WCSINFO** sur laquelle pointé *pWCSInfo* .</span><span class="sxs-lookup"><span data-stu-id="ae37a-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ae37a-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="ae37a-128">Remarks</span></span>

<span data-ttu-id="ae37a-129">**WrapCompressedRTFStreamEx** permet d’accéder au corps d’un message électronique encapsulé au format RTF compressé par décompression du flux, retourne le flux décompressé et son format et éventuellement le flux du corps native.</span><span class="sxs-lookup"><span data-stu-id="ae37a-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="ae37a-130">Le flux du corps native peut être dans le format RTF, texte brut ou HTML.</span><span class="sxs-lookup"><span data-stu-id="ae37a-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="ae37a-131">Le modèle objet Microsoft Office Outlook fournit une propriété **Body** pour les objets **MailItem** et d’une [Propriété MailItem.BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) qui indique le format du corps de texte.</span><span class="sxs-lookup"><span data-stu-id="ae37a-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="ae37a-132">Par leur conception, une solution qui n’est pas approuvée par Outlook appelle des boîtes de dialogue de sécurité générés par l’agent de sécurité Outlook.</span><span class="sxs-lookup"><span data-stu-id="ae37a-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="ae37a-133">À l’aide de la fonction MAPI exportée **WrapCompressedRTFStreamEx** permet une solution utilisent MAPI au lieu du modèle objet Outlook et d’éviter ces boîtes de dialogue de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ae37a-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="ae37a-134">Étant donné que la **MAPI\_NATIVE_BODY** indicateur ne peut être combiné avec la **MAPI\_modifier** indicateur dans le champ **ulFlags** de la **RTF\_WCSINFO** structure sur laquelle pointe *pWCSInfo*, vous pouvez uniquement accéder natif flux de corps en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ae37a-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="ae37a-135">Pour accéder au flux de corps native en mode lecture/écriture, vous devez utiliser la fonction **WrapCompressedRTFStream** .</span><span class="sxs-lookup"><span data-stu-id="ae37a-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae37a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae37a-136">See also</span></span>

- [<span data-ttu-id="ae37a-137">Récupérer le corps d’un message dans un fichier RTF compressé et le convertir dans son format natif</span><span class="sxs-lookup"><span data-stu-id="ae37a-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

