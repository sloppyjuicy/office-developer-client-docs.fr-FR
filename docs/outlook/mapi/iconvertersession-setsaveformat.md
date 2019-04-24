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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b528d6ef45c02b27f8e07d151793fc338f9af7b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336637"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="c90c0-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="c90c0-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="c90c0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c90c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c90c0-105">Définit le format dans lequel le convertisseur renverra un flux MIME dans [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="c90c0-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="c90c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c90c0-106">Parameters</span></span>

<span data-ttu-id="c90c0-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="c90c0-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="c90c0-108">dans Format d'enregistrement à utiliser pour un flux MIME.</span><span class="sxs-lookup"><span data-stu-id="c90c0-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="c90c0-109">Pour plus d'informations, voir le type d'énumération [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c90c0-109">For more information, see the enum type [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="c90c0-110">**SAVE_RFC1521**: utilisez MIME, qui est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c90c0-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="c90c0-111">**SAVE_RFC822**: utilisez uuencode.</span><span class="sxs-lookup"><span data-stu-id="c90c0-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c90c0-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c90c0-112">Return values</span></span>

<span data-ttu-id="c90c0-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c90c0-113">S_OK</span></span>
  
> <span data-ttu-id="c90c0-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="c90c0-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c90c0-115">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c90c0-115">MFCMAPI reference</span></span>

<span data-ttu-id="c90c0-116">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c90c0-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c90c0-117">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c90c0-117">**File**</span></span>|<span data-ttu-id="c90c0-118">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c90c0-118">**Function**</span></span>|<span data-ttu-id="c90c0-119">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c90c0-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c90c0-120">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="c90c0-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="c90c0-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="c90c0-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="c90c0-122">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="c90c0-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="c90c0-123">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="c90c0-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="c90c0-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="c90c0-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="c90c0-125">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.</span><span class="sxs-lookup"><span data-stu-id="c90c0-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c90c0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c90c0-126">See also</span></span>

- [<span data-ttu-id="c90c0-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c90c0-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="c90c0-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="c90c0-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="c90c0-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="c90c0-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="c90c0-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="c90c0-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="c90c0-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="c90c0-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="c90c0-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="c90c0-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="c90c0-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="c90c0-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="c90c0-134">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c90c0-134">MAPI Constants</span></span>](mapi-constants.md)

