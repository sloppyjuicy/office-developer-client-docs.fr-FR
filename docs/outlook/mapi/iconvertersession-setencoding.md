---
title: IConverterSessionSetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a13d4e54900989c692add85add6853a1b511f448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783666"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="0f7ff-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="0f7ff-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="0f7ff-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f7ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f7ff-105">Initialise le codage à utiliser lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="0f7ff-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="0f7ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f7ff-106">Parameters</span></span>

<span data-ttu-id="0f7ff-107">_et_</span><span class="sxs-lookup"><span data-stu-id="0f7ff-107">_et_</span></span>
  
> <span data-ttu-id="0f7ff-108">Une valeur [ENCODINGTYPE](http://msdn.microsoft.com/fr-fr/library/aa374936%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0f7ff-108">An [ENCODINGTYPE](http://msdn.microsoft.com/fr-fr/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="0f7ff-109">Uniquement les valeurs suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="0f7ff-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="0f7ff-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="0f7ff-110">IET_BASE64</span></span>
   - <span data-ttu-id="0f7ff-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="0f7ff-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="0f7ff-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="0f7ff-112">IET_QP</span></span>
   - <span data-ttu-id="0f7ff-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="0f7ff-113">IET_7BIT</span></span>
   - <span data-ttu-id="0f7ff-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="0f7ff-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f7ff-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="0f7ff-115">Return value</span></span>

<span data-ttu-id="0f7ff-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0f7ff-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="0f7ff-117">Le type de codage transmis n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="0f7ff-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f7ff-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f7ff-118">Remarks</span></span>

<span data-ttu-id="0f7ff-119">Appelez **SetEncoding** avant d’utiliser [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="0f7ff-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="0f7ff-120">Utilisez **SetEncoding** pour définir le codage pour seulement le corps du message extérieur d’un élément de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0f7ff-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="0f7ff-121">Microsoft Outlook 2010 et Microsoft Outlook 2013 choisissent le codage pour les pièces jointes individuels.</span><span class="sxs-lookup"><span data-stu-id="0f7ff-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0f7ff-122">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0f7ff-122">MFCMAPI reference</span></span>

<span data-ttu-id="0f7ff-123">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0f7ff-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0f7ff-124">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="0f7ff-124">**File**</span></span>|<span data-ttu-id="0f7ff-125">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="0f7ff-125">**Function**</span></span>|<span data-ttu-id="0f7ff-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="0f7ff-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0f7ff-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="0f7ff-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="0f7ff-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="0f7ff-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="0f7ff-129">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f7ff-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="0f7ff-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="0f7ff-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="0f7ff-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="0f7ff-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="0f7ff-132">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.</span><span class="sxs-lookup"><span data-stu-id="0f7ff-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f7ff-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f7ff-133">See also</span></span>

- [<span data-ttu-id="0f7ff-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f7ff-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="0f7ff-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="0f7ff-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="0f7ff-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="0f7ff-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="0f7ff-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="0f7ff-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="0f7ff-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="0f7ff-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="0f7ff-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="0f7ff-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="0f7ff-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="0f7ff-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="0f7ff-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0f7ff-141">MAPI Constants</span></span>](mapi-constants.md)

