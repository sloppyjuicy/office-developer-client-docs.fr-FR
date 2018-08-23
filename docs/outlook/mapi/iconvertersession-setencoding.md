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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3edcb422eb0e3dd415d49c5e014c8b69095e7ec1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577204"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="905d2-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="905d2-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="905d2-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="905d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="905d2-105">Initialise le codage à utiliser lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="905d2-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="905d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="905d2-106">Parameters</span></span>

<span data-ttu-id="905d2-107">_et_</span><span class="sxs-lookup"><span data-stu-id="905d2-107">_et_</span></span>
  
> <span data-ttu-id="905d2-108">Une valeur [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="905d2-108">An [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="905d2-109">Uniquement les valeurs suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="905d2-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="905d2-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="905d2-110">IET_BASE64</span></span>
   - <span data-ttu-id="905d2-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="905d2-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="905d2-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="905d2-112">IET_QP</span></span>
   - <span data-ttu-id="905d2-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="905d2-113">IET_7BIT</span></span>
   - <span data-ttu-id="905d2-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="905d2-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="905d2-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="905d2-115">Return value</span></span>

<span data-ttu-id="905d2-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="905d2-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="905d2-117">Le type de codage transmis n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="905d2-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="905d2-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="905d2-118">Remarks</span></span>

<span data-ttu-id="905d2-119">Appelez **SetEncoding** avant d’utiliser [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="905d2-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="905d2-120">Utilisez **SetEncoding** pour définir le codage pour seulement le corps du message extérieur d’un élément de messagerie.</span><span class="sxs-lookup"><span data-stu-id="905d2-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="905d2-121">Microsoft Outlook 2010 et Microsoft Outlook 2013 choisissent le codage pour les pièces jointes individuels.</span><span class="sxs-lookup"><span data-stu-id="905d2-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="905d2-122">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="905d2-122">MFCMAPI reference</span></span>

<span data-ttu-id="905d2-123">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="905d2-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="905d2-124">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="905d2-124">**File**</span></span>|<span data-ttu-id="905d2-125">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="905d2-125">**Function**</span></span>|<span data-ttu-id="905d2-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="905d2-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="905d2-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="905d2-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="905d2-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="905d2-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="905d2-129">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="905d2-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="905d2-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="905d2-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="905d2-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="905d2-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="905d2-132">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.</span><span class="sxs-lookup"><span data-stu-id="905d2-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="905d2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="905d2-133">See also</span></span>

- [<span data-ttu-id="905d2-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="905d2-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="905d2-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="905d2-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="905d2-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="905d2-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="905d2-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="905d2-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="905d2-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="905d2-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="905d2-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="905d2-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="905d2-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="905d2-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="905d2-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="905d2-141">MAPI Constants</span></span>](mapi-constants.md)

