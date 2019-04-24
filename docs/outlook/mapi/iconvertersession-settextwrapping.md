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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336630"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="89d20-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="89d20-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="89d20-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89d20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89d20-105">Définit la largeur de l'habillage du texte pour un flux MIME que le convertisseur renverra dans [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="89d20-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="89d20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89d20-106">Parameters</span></span>

 <span data-ttu-id="89d20-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="89d20-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="89d20-108">dans Indique si le texte doit être renvoyé à la ligne ou non.</span><span class="sxs-lookup"><span data-stu-id="89d20-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="89d20-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="89d20-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="89d20-110">dans Largeur de l'habillage du texte à utiliser.</span><span class="sxs-lookup"><span data-stu-id="89d20-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="89d20-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89d20-111">Return value</span></span>

<span data-ttu-id="89d20-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="89d20-112">S_OK</span></span>
  
> <span data-ttu-id="89d20-113">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="89d20-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="89d20-114">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="89d20-114">MFCMAPI reference</span></span>

<span data-ttu-id="89d20-115">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="89d20-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="89d20-116">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="89d20-116">**File**</span></span>|<span data-ttu-id="89d20-117">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="89d20-117">**Function**</span></span>|<span data-ttu-id="89d20-118">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="89d20-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89d20-119">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="89d20-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="89d20-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="89d20-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="89d20-121">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="89d20-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="89d20-122">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="89d20-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="89d20-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="89d20-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="89d20-124">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.</span><span class="sxs-lookup"><span data-stu-id="89d20-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89d20-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89d20-125">See also</span></span>



[<span data-ttu-id="89d20-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89d20-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="89d20-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="89d20-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="89d20-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="89d20-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="89d20-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="89d20-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="89d20-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="89d20-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="89d20-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="89d20-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="89d20-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="89d20-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="89d20-133">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="89d20-133">MAPI Constants</span></span>](mapi-constants.md)

