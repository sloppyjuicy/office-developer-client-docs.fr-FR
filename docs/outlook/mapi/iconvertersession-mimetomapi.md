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
ms.openlocfilehash: 356f4470be26ae3803a53af1cec34b3ac6eb0cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326928"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="9e821-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="9e821-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="9e821-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e821-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e821-105">ConVertit un flux MIME en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e821-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="9e821-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e821-106">Parameters</span></span>

 <span data-ttu-id="9e821-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="9e821-107">_pstm_</span></span>
  
> <span data-ttu-id="9e821-108">dans Interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) à un flux MIME.</span><span class="sxs-lookup"><span data-stu-id="9e821-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="9e821-109">_PMSG_</span><span class="sxs-lookup"><span data-stu-id="9e821-109">_pmsg_</span></span>
  
> <span data-ttu-id="9e821-110">remarquer Pointeur vers le message à charger.</span><span class="sxs-lookup"><span data-stu-id="9e821-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="9e821-111">Voir mapidefs. h pour la définition de type de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="9e821-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="9e821-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="9e821-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="9e821-113">dans Cette valeur doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="9e821-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="9e821-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e821-114">_ulFlags_</span></span>
  
> <span data-ttu-id="9e821-115">dans Ce paramètre identifie toute action spéciale à effectuer lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="9e821-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="9e821-116">Elle doit être égale à zéro (0) si aucune action spécifique n'est effectuée, ou une combinaison des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="9e821-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="9e821-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="9e821-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="9e821-118">Les informations envoyées/non envoyées sont conservées dans X-non envoyés.</span><span class="sxs-lookup"><span data-stu-id="9e821-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="9e821-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="9e821-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="9e821-120">Le flux MIME est destiné à un message SMTP (simple MAPI Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="9e821-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="9e821-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="9e821-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="9e821-122">Les destinataires en copie carbone invisible du flux MIME doivent être inclus dans le message MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e821-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="9e821-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="9e821-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="9e821-124">Le corps HTML du flux MIME doit être converti au format RTF (Rich Text Format) dans le message MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e821-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="9e821-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="9e821-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="9e821-126">Le convertisseur doit gérer le flux MIME en tant que message international (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="9e821-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="9e821-127">Non pris en charge sur Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="9e821-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e821-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9e821-128">Return value</span></span>

<span data-ttu-id="9e821-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9e821-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="9e821-130">Indique que _pstm_ est **null**, _PMSG_ est **null**ou _ulFlags_ n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9e821-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e821-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="9e821-131">Remarks</span></span>

<span data-ttu-id="9e821-132">Si vous avez spécifié **CCSF_USE_RTF** dans le cadre de _ulFlags_ et que la Banque de messages de destination prend en charge à la fois le format HTML et le format RTF, le message MAPI est converti au format HTML ou RTF.</span><span class="sxs-lookup"><span data-stu-id="9e821-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="9e821-133">Si le message est converti au format RTF, le format converti sera au format RTF compressé, tous les éléments HTML seront incorporés dans la chaîne RTF compressée, et la chaîne sera contenue dans la [propriété canonique PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="9e821-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9e821-134">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9e821-134">MFCMAPI reference</span></span>

<span data-ttu-id="9e821-135">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9e821-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9e821-136">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="9e821-136">**File**</span></span>|<span data-ttu-id="9e821-137">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="9e821-137">**Function**</span></span>|<span data-ttu-id="9e821-138">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="9e821-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e821-139">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="9e821-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="9e821-140">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="9e821-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="9e821-141">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e821-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="9e821-142">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="9e821-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="9e821-143">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="9e821-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="9e821-144">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.</span><span class="sxs-lookup"><span data-stu-id="9e821-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e821-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e821-145">See also</span></span>



[<span data-ttu-id="9e821-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e821-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="9e821-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="9e821-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="9e821-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="9e821-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="9e821-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="9e821-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="9e821-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="9e821-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="9e821-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="9e821-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="9e821-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="9e821-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="9e821-153">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9e821-153">MAPI Constants</span></span>](mapi-constants.md)

