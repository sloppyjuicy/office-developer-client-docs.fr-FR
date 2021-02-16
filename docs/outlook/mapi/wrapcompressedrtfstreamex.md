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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325773"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="f10f4-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="f10f4-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="f10f4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f10f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f10f4-105">Décompresse le corps d’un message électronique au format RTF (Compressed Rich Text Format), indique le format du flux décompressé, convertit éventuellement le flux décompressé en son format natif et renvoie le flux décompressé ou le flux natif converti.</span><span class="sxs-lookup"><span data-stu-id="f10f4-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f10f4-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f10f4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f10f4-107">Exporté par :</span><span class="sxs-lookup"><span data-stu-id="f10f4-107">Exported by:</span></span>  <br/> |<span data-ttu-id="f10f4-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="f10f4-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="f10f4-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f10f4-109">Called by:</span></span>  <br/> |<span data-ttu-id="f10f4-110">Client</span><span class="sxs-lookup"><span data-stu-id="f10f4-110">Client</span></span>  <br/> |
|<span data-ttu-id="f10f4-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f10f4-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="f10f4-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="f10f4-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="f10f4-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f10f4-113">Parameters</span></span>

<span data-ttu-id="f10f4-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f10f4-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="f10f4-115">[in] Il s’agit d’un pointeur vers un flux ouvert sur la propriété canonique [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) d’un message.</span><span class="sxs-lookup"><span data-stu-id="f10f4-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="f10f4-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="f10f4-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="f10f4-117">[in] Il s’agit d’un pointeur vers un</span><span class="sxs-lookup"><span data-stu-id="f10f4-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="f10f4-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure qui contient les options de la fonction.</span><span class="sxs-lookup"><span data-stu-id="f10f4-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="f10f4-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="f10f4-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="f10f4-120">[out] Il s’agit d’un pointeur vers l’emplacement où un flux pour le RTF décompressé est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="f10f4-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="f10f4-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="f10f4-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="f10f4-122">[out] Il s’agit d’un [pointeur vers une](rtf_wcsretinfo.md) structure RTF_WCSRETINFO qui contient des informations sur le format du flux décompressé renvoyé.</span><span class="sxs-lookup"><span data-stu-id="f10f4-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f10f4-123">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f10f4-123">Return values</span></span>

<span data-ttu-id="f10f4-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f10f4-124">S_OK</span></span> 
  
- <span data-ttu-id="f10f4-125">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="f10f4-125">The function call is successful.</span></span>
    
<span data-ttu-id="f10f4-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f10f4-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="f10f4-127">Ceci est renvoyé si **l’indicateur MAPI_NATIVE_BODY** est combiné avec l’indicateur **MAPI_MODIFY** dans le champ **ulFlags** de la structure **RTF_WCSINFO** pointée par  *pWCSInfo*  .</span><span class="sxs-lookup"><span data-stu-id="f10f4-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f10f4-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="f10f4-128">Remarks</span></span>

<span data-ttu-id="f10f4-129">**WrapCompressedRTFStreamEx** vous permet d’accéder au corps d’un message électronique encapsulé dans un format RTF compressé en décompressant le flux, renvoie le flux décompressé et son format, et éventuellement le flux de corps natif.</span><span class="sxs-lookup"><span data-stu-id="f10f4-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="f10f4-130">Le flux de corps natif peut être au format RTF, en texte brut ou au format HTML.</span><span class="sxs-lookup"><span data-stu-id="f10f4-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="f10f4-131">Le Microsoft Office Outlook objet fournit une propriété **Body** pour les objets **MailItem** et une [propriété MailItem.BodyFormat (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) qui indique le format du corps de texte.</span><span class="sxs-lookup"><span data-stu-id="f10f4-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="f10f4-132">Par conception, une solution non fiable par Outlook appelle les boîtes de dialogue de sécurité générées par Outlook Security Guard.</span><span class="sxs-lookup"><span data-stu-id="f10f4-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="f10f4-133">L’utilisation de la fonction MAPI **exportée WrapCompressedRTFStreamEx** permet à une solution d’utiliser MAPI au lieu du modèle objet Outlook et d’éviter ces boîtes de dialogue de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f10f4-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="f10f4-134">Étant donné que l’indicateur **\_ NATIVE_BODY MAPI** ne peut pas être combiné avec l’indicateur **MAPI \_ MODIFY** dans le champ **ulFlags** de la structure **\_ WCSINFO RTF** pointée par *pWCSInfo,* vous pouvez uniquement accéder au flux de corps natif en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f10f4-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="f10f4-135">Pour accéder au flux de corps natif en mode lecture/écriture, vous devez utiliser la fonction **WrapCompressedRTFStream.**</span><span class="sxs-lookup"><span data-stu-id="f10f4-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f10f4-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f10f4-136">See also</span></span>

- [<span data-ttu-id="f10f4-137">Récupérer le corps d’un message au format RTF compressé et le convertir au format natif</span><span class="sxs-lookup"><span data-stu-id="f10f4-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

