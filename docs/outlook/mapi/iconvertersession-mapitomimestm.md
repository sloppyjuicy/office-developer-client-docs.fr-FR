---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Dernière modification : 20 septembre 2017'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400116"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="beb6b-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="beb6b-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="beb6b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="beb6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="beb6b-105">Convertit un message MAPI à un flux de données MIME.</span><span class="sxs-lookup"><span data-stu-id="beb6b-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="beb6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="beb6b-106">Parameters</span></span>

 <span data-ttu-id="beb6b-107">_pMsg_</span><span class="sxs-lookup"><span data-stu-id="beb6b-107">_pmsg_</span></span>
  
> <span data-ttu-id="beb6b-108">[in] Pointeur vers le message à convertir.</span><span class="sxs-lookup"><span data-stu-id="beb6b-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="beb6b-109">Voir mapidefs.h pour la définition du type de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="beb6b-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="beb6b-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="beb6b-110">_pstm_</span></span>
  
> <span data-ttu-id="beb6b-111">[out] Interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) pour le flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="beb6b-111">[out] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="beb6b-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="beb6b-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="beb6b-113">[in] Indicateurs qui indiquent des actions spécifiques pour le convertisseur :</span><span class="sxs-lookup"><span data-stu-id="beb6b-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="beb6b-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="beb6b-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="beb6b-115">Le convertisseur doit permettre d’en-têtes de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="beb6b-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="beb6b-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="beb6b-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="beb6b-117">Informations envoyées/en attente ne sont conservées dans X-en attente.</span><span class="sxs-lookup"><span data-stu-id="beb6b-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="beb6b-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="beb6b-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="beb6b-119">Le convertisseur doit générer un message international (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="beb6b-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="beb6b-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="beb6b-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="beb6b-121">Les destinataires Cci du message MAPI doivent être inclus dans le flux MIME.</span><span class="sxs-lookup"><span data-stu-id="beb6b-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="beb6b-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="beb6b-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="beb6b-123">N’incluez pas le champ Id de Message dans les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="beb6b-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="beb6b-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="beb6b-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="beb6b-125">Le convertisseur doit ignorer les en-têtes du message extérieur.</span><span class="sxs-lookup"><span data-stu-id="beb6b-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="beb6b-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="beb6b-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="beb6b-127">Le convertisseur doit envoyer du texte brut.</span><span class="sxs-lookup"><span data-stu-id="beb6b-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="beb6b-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="beb6b-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="beb6b-129">Le convertisseur est passé un message SMTP.</span><span class="sxs-lookup"><span data-stu-id="beb6b-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="beb6b-130">Cet indicateur doit toujours être défini.</span><span class="sxs-lookup"><span data-stu-id="beb6b-130">This flag must always be set.</span></span>
    
<span data-ttu-id="beb6b-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="beb6b-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="beb6b-132">Le convertisseur doit convertir au format RTF dans le message MIME HTML.</span><span class="sxs-lookup"><span data-stu-id="beb6b-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="beb6b-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="beb6b-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="beb6b-134">Le convertisseur doit utiliser le format TNEF Transport Neutral Encapsulation Format () dans le message MIME.</span><span class="sxs-lookup"><span data-stu-id="beb6b-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="beb6b-135">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="beb6b-135">Return values</span></span>

<span data-ttu-id="beb6b-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beb6b-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="beb6b-137">Indicateurs non valides ont été passés ou *pmsg* ou *pstm* est NULL.</span><span class="sxs-lookup"><span data-stu-id="beb6b-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="beb6b-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="beb6b-138">Remarks</span></span>

<span data-ttu-id="beb6b-139">Prise en charge uniquement pour les types de message Outlook standard.</span><span class="sxs-lookup"><span data-stu-id="beb6b-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="beb6b-140">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="beb6b-140">MFCMAPI reference</span></span>

<span data-ttu-id="beb6b-141">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="beb6b-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="beb6b-142">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="beb6b-142">**File**</span></span>|<span data-ttu-id="beb6b-143">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="beb6b-143">**Function**</span></span>|<span data-ttu-id="beb6b-144">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="beb6b-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="beb6b-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="beb6b-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="beb6b-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="beb6b-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="beb6b-147">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="beb6b-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="beb6b-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="beb6b-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="beb6b-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="beb6b-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="beb6b-150">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.</span><span class="sxs-lookup"><span data-stu-id="beb6b-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="beb6b-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="beb6b-151">See also</span></span>



[<span data-ttu-id="beb6b-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="beb6b-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="beb6b-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="beb6b-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="beb6b-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="beb6b-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="beb6b-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="beb6b-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="beb6b-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="beb6b-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="beb6b-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="beb6b-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="beb6b-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="beb6b-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="beb6b-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="beb6b-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="beb6b-160">Propriété canonique PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="beb6b-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="beb6b-161">Propriété canonique PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="beb6b-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="beb6b-162">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="beb6b-162">MAPI Constants</span></span>](mapi-constants.md)

