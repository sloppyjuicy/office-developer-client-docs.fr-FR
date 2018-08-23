---
title: IConverterSessionSetSaveFormat
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
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f24ad938fdb8c3ac234e1d78f2668139840c8b8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568216"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="ef8a7-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="ef8a7-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="ef8a7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef8a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef8a7-105">Définit le format dans lequel le convertisseur retournera un flux MIME dans [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="ef8a7-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="ef8a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef8a7-106">Parameters</span></span>

<span data-ttu-id="ef8a7-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="ef8a7-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="ef8a7-108">[in] Format d’enregistrement à utiliser pour un flux de données MIME.</span><span class="sxs-lookup"><span data-stu-id="ef8a7-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="ef8a7-109">Pour plus d’informations, voir le type enum [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef8a7-109">For more information, see the enum type [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="ef8a7-110">**SAVE_RFC1521**: utiliser MIME, qui est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ef8a7-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="ef8a7-111">**SAVE_RFC822**: utiliser uuencode.</span><span class="sxs-lookup"><span data-stu-id="ef8a7-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ef8a7-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ef8a7-112">Return values</span></span>

<span data-ttu-id="ef8a7-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef8a7-113">S_OK</span></span>
  
> <span data-ttu-id="ef8a7-114">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="ef8a7-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ef8a7-115">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ef8a7-115">MFCMAPI reference</span></span>

<span data-ttu-id="ef8a7-116">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ef8a7-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ef8a7-117">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ef8a7-117">**File**</span></span>|<span data-ttu-id="ef8a7-118">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ef8a7-118">**Function**</span></span>|<span data-ttu-id="ef8a7-119">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ef8a7-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef8a7-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ef8a7-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ef8a7-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="ef8a7-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="ef8a7-122">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="ef8a7-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="ef8a7-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ef8a7-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ef8a7-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="ef8a7-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="ef8a7-125">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.</span><span class="sxs-lookup"><span data-stu-id="ef8a7-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef8a7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef8a7-126">See also</span></span>

- [<span data-ttu-id="ef8a7-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef8a7-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="ef8a7-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="ef8a7-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="ef8a7-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="ef8a7-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="ef8a7-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="ef8a7-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="ef8a7-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="ef8a7-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="ef8a7-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="ef8a7-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="ef8a7-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="ef8a7-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="ef8a7-134">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ef8a7-134">MAPI Constants</span></span>](mapi-constants.md)

