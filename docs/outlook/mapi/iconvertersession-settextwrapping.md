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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a89f6dd14e8bbea9d0d4145dc05bf332af95234a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573631"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="59351-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="59351-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="59351-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59351-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59351-105">Définit la largeur d’un flux MIME qui renverra le convertisseur [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)d’habillage de texte.</span><span class="sxs-lookup"><span data-stu-id="59351-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="59351-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59351-106">Parameters</span></span>

 <span data-ttu-id="59351-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="59351-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="59351-108">[in] S’il faut répartir le texte ou non.</span><span class="sxs-lookup"><span data-stu-id="59351-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="59351-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="59351-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="59351-110">[in] L’habillage largeur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="59351-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59351-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="59351-111">Return value</span></span>

<span data-ttu-id="59351-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="59351-112">S_OK</span></span>
  
> <span data-ttu-id="59351-113">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="59351-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="59351-114">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="59351-114">MFCMAPI reference</span></span>

<span data-ttu-id="59351-115">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="59351-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="59351-116">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="59351-116">**File**</span></span>|<span data-ttu-id="59351-117">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="59351-117">**Function**</span></span>|<span data-ttu-id="59351-118">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="59351-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59351-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="59351-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="59351-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="59351-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="59351-121">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="59351-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="59351-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="59351-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="59351-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="59351-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="59351-124">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.</span><span class="sxs-lookup"><span data-stu-id="59351-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59351-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59351-125">See also</span></span>



[<span data-ttu-id="59351-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="59351-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="59351-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="59351-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="59351-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="59351-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="59351-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="59351-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="59351-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="59351-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="59351-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="59351-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="59351-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="59351-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="59351-133">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="59351-133">MAPI Constants</span></span>](mapi-constants.md)

