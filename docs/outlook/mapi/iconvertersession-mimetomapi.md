---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 03a67371c67d5f0ac346470ec7ab38bb67d5ce2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19783654"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="c1fc8-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="c1fc8-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="c1fc8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1fc8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1fc8-105">Convertit un flux de données MIME à un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="c1fc8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1fc8-106">Parameters</span></span>

 <span data-ttu-id="c1fc8-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="c1fc8-107">_pstm_</span></span>
  
> <span data-ttu-id="c1fc8-108">[in] Interface [IStream](http://msdn.microsoft.com/fr-fr/library/aa380034%28VS.85%29.aspx) pour un flux de données MIME.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-108">[in] [IStream](http://msdn.microsoft.com/fr-fr/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="c1fc8-109">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="c1fc8-109">_pmsg_</span></span>
  
> <span data-ttu-id="c1fc8-110">[out] Pointeur vers le message à charger.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="c1fc8-111">Voir mapidefs.h pour la définition du type de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="c1fc8-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="c1fc8-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="c1fc8-113">[in] Cette valeur doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="c1fc8-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1fc8-114">_ulFlags_</span></span>
  
> <span data-ttu-id="c1fc8-115">[in] Ce paramètre identifie l’action particulière à prendre lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="c1fc8-116">Il doit être égal à zéro (0) si aucune action n’est prise en ou une combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c1fc8-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="c1fc8-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c1fc8-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="c1fc8-118">Informations envoyées/en attente ne sont conservées dans X-en attente.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="c1fc8-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="c1fc8-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="c1fc8-120">Le flux MIME est un message Simple MAPI Transfer Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="c1fc8-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="c1fc8-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="c1fc8-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="c1fc8-122">Les destinataires Cci du flux MIME doivent être inclus dans le message MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="c1fc8-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="c1fc8-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="c1fc8-124">Le corps HTML de l’objet stream MIME doivent être converti au Format RTF (RICH Text Format) dans le message MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1fc8-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c1fc8-125">Return value</span></span>

<span data-ttu-id="c1fc8-126">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c1fc8-126">E_INVALIDARG</span></span>
  
> <span data-ttu-id="c1fc8-127">Indique que _pstm_ a la **valeur null**, _pmsg_ est **null**ou _ulFlags_ n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-127">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c1fc8-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1fc8-128">Remarks</span></span>

<span data-ttu-id="c1fc8-129">Si vous avez spécifié **CCSF_USE_RTF** dans le cadre de _ulFlags_ et la banque de messages de destination prend en charge HTML et RTF, le message MAPI est converti au format HTML ou RTF.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-129">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="c1fc8-130">Si le message est converti au format RTF, au format converti est compressé au format RTF, HTML sera incorporée dans la chaîne de format RTF compressée, et la chaîne figure dans la [Propriété canonique PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="c1fc8-130">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c1fc8-131">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c1fc8-131">MFCMAPI reference</span></span>

<span data-ttu-id="c1fc8-132">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c1fc8-133">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c1fc8-133">**File**</span></span>|<span data-ttu-id="c1fc8-134">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c1fc8-134">**Function**</span></span>|<span data-ttu-id="c1fc8-135">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c1fc8-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1fc8-136">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="c1fc8-136">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="c1fc8-137">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="c1fc8-137">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="c1fc8-138">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-138">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="c1fc8-139">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="c1fc8-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="c1fc8-140">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="c1fc8-140">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="c1fc8-141">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-141">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1fc8-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1fc8-142">See also</span></span>



[<span data-ttu-id="c1fc8-143">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1fc8-143">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="c1fc8-144">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="c1fc8-144">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="c1fc8-145">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="c1fc8-145">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="c1fc8-146">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="c1fc8-146">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="c1fc8-147">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="c1fc8-147">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="c1fc8-148">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="c1fc8-148">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="c1fc8-149">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="c1fc8-149">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="c1fc8-150">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c1fc8-150">MAPI Constants</span></span>](mapi-constants.md)

