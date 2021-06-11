---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423586"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="6c2f2-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="6c2f2-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="6c2f2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c2f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c2f2-105">Définit la largeur du retour à la ligne pour un flux MIME que le convertisseur retournera dans [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="6c2f2-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="6c2f2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6c2f2-106">Parameters</span></span>

 <span data-ttu-id="6c2f2-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="6c2f2-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="6c2f2-108">[in] S’il faut encapsuler le texte ou non.</span><span class="sxs-lookup"><span data-stu-id="6c2f2-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="6c2f2-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="6c2f2-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="6c2f2-110">[in] Largeur du habillage de texte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6c2f2-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c2f2-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6c2f2-111">Return value</span></span>

<span data-ttu-id="6c2f2-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c2f2-112">S_OK</span></span>
  
> <span data-ttu-id="6c2f2-113">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="6c2f2-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="6c2f2-114">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6c2f2-114">MFCMAPI reference</span></span>

<span data-ttu-id="6c2f2-115">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6c2f2-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6c2f2-116">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6c2f2-116">**File**</span></span>|<span data-ttu-id="6c2f2-117">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6c2f2-117">**Function**</span></span>|<span data-ttu-id="6c2f2-118">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6c2f2-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c2f2-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="6c2f2-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="6c2f2-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="6c2f2-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="6c2f2-121">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="6c2f2-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="6c2f2-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="6c2f2-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="6c2f2-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="6c2f2-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="6c2f2-124">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.</span><span class="sxs-lookup"><span data-stu-id="6c2f2-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c2f2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c2f2-125">See also</span></span>



[<span data-ttu-id="6c2f2-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c2f2-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="6c2f2-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="6c2f2-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="6c2f2-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="6c2f2-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="6c2f2-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="6c2f2-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="6c2f2-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="6c2f2-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="6c2f2-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="6c2f2-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="6c2f2-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="6c2f2-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="6c2f2-133">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6c2f2-133">MAPI Constants</span></span>](mapi-constants.md)

