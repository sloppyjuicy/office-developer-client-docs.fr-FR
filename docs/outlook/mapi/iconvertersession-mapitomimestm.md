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
description: 'Last modified: September 20, 2017'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326943"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="a5978-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="a5978-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="a5978-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5978-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5978-105">Convertit un message MAPI en flux MIME.</span><span class="sxs-lookup"><span data-stu-id="a5978-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="a5978-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5978-106">Parameters</span></span>

 <span data-ttu-id="a5978-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="a5978-107">_pmsg_</span></span>
  
> <span data-ttu-id="a5978-108">[in] Pointeur vers le message à convertir.</span><span class="sxs-lookup"><span data-stu-id="a5978-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="a5978-109">Voir mapidefs.h pour la définition de type **de LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="a5978-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="a5978-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="a5978-110">_pstm_</span></span>
  
> <span data-ttu-id="a5978-111">[out] [Interface IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) pour la sortie du flux.</span><span class="sxs-lookup"><span data-stu-id="a5978-111">[out] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="a5978-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5978-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="a5978-113">[in] Indicateurs qui indiquent des actions spécifiques pour le convertisseur :</span><span class="sxs-lookup"><span data-stu-id="a5978-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="a5978-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="a5978-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="a5978-115">Le convertisseur doit autoriser les en-têtes 8 bits.</span><span class="sxs-lookup"><span data-stu-id="a5978-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="a5978-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a5978-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="a5978-117">Les informations envoyées/non envoyées sont persistantes dans X-Unsent.</span><span class="sxs-lookup"><span data-stu-id="a5978-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="a5978-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a5978-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="a5978-119">Le convertisseur doit créer un message international (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="a5978-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="a5978-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="a5978-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="a5978-121">Les destinataires Bc du message MAPI doivent être inclus dans le flux MIME.</span><span class="sxs-lookup"><span data-stu-id="a5978-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="a5978-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="a5978-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="a5978-123">N’incluez pas Message-Id champ dans les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="a5978-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="a5978-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="a5978-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="a5978-125">Le convertisseur doit ignorer les en-têtes du message externe.</span><span class="sxs-lookup"><span data-stu-id="a5978-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="a5978-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="a5978-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="a5978-127">Le convertisseur doit simplement envoyer du texte simple.</span><span class="sxs-lookup"><span data-stu-id="a5978-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="a5978-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="a5978-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="a5978-129">Un message SMTP est transmis au convertisseur.</span><span class="sxs-lookup"><span data-stu-id="a5978-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="a5978-130">Cet indicateur doit toujours être définie.</span><span class="sxs-lookup"><span data-stu-id="a5978-130">This flag must always be set.</span></span>
    
<span data-ttu-id="a5978-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="a5978-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="a5978-132">Le convertisseur doit convertir du format HTML au format RTF dans le message MIME.</span><span class="sxs-lookup"><span data-stu-id="a5978-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="a5978-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="a5978-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="a5978-134">Le convertisseur doit utiliser le format TNEF (Transport Neutral Encapsulation Format) dans le message MIME.</span><span class="sxs-lookup"><span data-stu-id="a5978-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a5978-135">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a5978-135">Return values</span></span>

<span data-ttu-id="a5978-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a5978-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="a5978-137">Des indicateurs non valides ont été passés ou  *pmsg*  ou  *pstm*  a la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="a5978-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a5978-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5978-138">Remarks</span></span>

<span data-ttu-id="a5978-139">Pris en charge uniquement pour les types de messages Outlook standard.</span><span class="sxs-lookup"><span data-stu-id="a5978-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a5978-140">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a5978-140">MFCMAPI reference</span></span>

<span data-ttu-id="a5978-141">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a5978-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a5978-142">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="a5978-142">**File**</span></span>|<span data-ttu-id="a5978-143">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a5978-143">**Function**</span></span>|<span data-ttu-id="a5978-144">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a5978-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a5978-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="a5978-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="a5978-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="a5978-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="a5978-147">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="a5978-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="a5978-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="a5978-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="a5978-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="a5978-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="a5978-150">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.</span><span class="sxs-lookup"><span data-stu-id="a5978-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5978-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5978-151">See also</span></span>



[<span data-ttu-id="a5978-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5978-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="a5978-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="a5978-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="a5978-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="a5978-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="a5978-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="a5978-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="a5978-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="a5978-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="a5978-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="a5978-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="a5978-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="a5978-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="a5978-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="a5978-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="a5978-160">Propriété canonique PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="a5978-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="a5978-161">Propri�t� canonique PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="a5978-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="a5978-162">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a5978-162">MAPI Constants</span></span>](mapi-constants.md)

