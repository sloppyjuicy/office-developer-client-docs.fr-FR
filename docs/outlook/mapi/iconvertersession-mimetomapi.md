---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Dernière modification : septembre 06, 2019'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160285"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="e36ab-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="e36ab-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="e36ab-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e36ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e36ab-105">Convertit un flux MIME en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="e36ab-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="e36ab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e36ab-106">Parameters</span></span>

 <span data-ttu-id="e36ab-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="e36ab-107">_pstm_</span></span>
  
> <span data-ttu-id="e36ab-108">dans Interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) à un flux MIME.</span><span class="sxs-lookup"><span data-stu-id="e36ab-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="e36ab-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="e36ab-109">_pmsg_</span></span>
  
> <span data-ttu-id="e36ab-110">dans Pointeur vers le message à charger.</span><span class="sxs-lookup"><span data-stu-id="e36ab-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="e36ab-111">L’appelant doit fournir un message pour que l’API le remplisse, afin que l’objet soit placé [in].</span><span class="sxs-lookup"><span data-stu-id="e36ab-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="e36ab-112">Voir mapidefs. h pour la définition de type de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="e36ab-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="e36ab-113">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="e36ab-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="e36ab-114">dans Cette valeur doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="e36ab-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="e36ab-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e36ab-115">_ulFlags_</span></span>
  
> <span data-ttu-id="e36ab-116">dans Ce paramètre identifie toute action spéciale à effectuer lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="e36ab-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="e36ab-117">Elle doit être égale à zéro (0) si aucune action spécifique n’est effectuée, ou une combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e36ab-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="e36ab-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="e36ab-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="e36ab-119">Les informations envoyées/non envoyées sont conservées dans X-non envoyés.</span><span class="sxs-lookup"><span data-stu-id="e36ab-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="e36ab-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="e36ab-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="e36ab-121">Le flux MIME est destiné à un message SMTP (Simple Mail Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="e36ab-121">The MIME stream is for a Simple Mail Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="e36ab-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="e36ab-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="e36ab-123">Les destinataires en copie carbone invisible du flux MIME doivent être inclus dans le message MAPI.</span><span class="sxs-lookup"><span data-stu-id="e36ab-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="e36ab-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="e36ab-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="e36ab-125">Le corps HTML du flux MIME doit être converti au format RTF (Rich Text Format) dans le message MAPI.</span><span class="sxs-lookup"><span data-stu-id="e36ab-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="e36ab-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="e36ab-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="e36ab-127">Le convertisseur doit gérer le flux MIME en tant que message international (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="e36ab-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="e36ab-128">Non pris en charge sur Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="e36ab-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e36ab-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e36ab-129">Return value</span></span>

<span data-ttu-id="e36ab-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e36ab-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="e36ab-131">Indique que _pstm_ est **null**, _PMSG_ est **null**ou _ulFlags_ n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e36ab-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e36ab-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="e36ab-132">Remarks</span></span>

<span data-ttu-id="e36ab-133">Si vous avez spécifié **CCSF_USE_RTF** dans le cadre de _ulFlags_ et que la Banque de messages de destination prend en charge à la fois le format HTML et le format RTF, le message MAPI est converti au format HTML ou RTF.</span><span class="sxs-lookup"><span data-stu-id="e36ab-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="e36ab-134">Si le message est converti au format RTF, le format converti sera au format RTF compressé, tous les éléments HTML seront incorporés dans la chaîne RTF compressée, et la chaîne sera contenue dans la [propriété canonique PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="e36ab-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e36ab-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e36ab-135">MFCMAPI reference</span></span>

<span data-ttu-id="e36ab-136">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e36ab-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e36ab-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e36ab-137">**File**</span></span>|<span data-ttu-id="e36ab-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e36ab-138">**Function**</span></span>|<span data-ttu-id="e36ab-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e36ab-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e36ab-140">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="e36ab-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e36ab-141">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="e36ab-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="e36ab-142">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="e36ab-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="e36ab-143">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="e36ab-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e36ab-144">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="e36ab-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="e36ab-145">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.</span><span class="sxs-lookup"><span data-stu-id="e36ab-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e36ab-146">Consultez également</span><span class="sxs-lookup"><span data-stu-id="e36ab-146">See also</span></span>



[<span data-ttu-id="e36ab-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e36ab-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="e36ab-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="e36ab-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="e36ab-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="e36ab-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="e36ab-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="e36ab-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="e36ab-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="e36ab-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="e36ab-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="e36ab-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="e36ab-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="e36ab-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="e36ab-154">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e36ab-154">MAPI Constants</span></span>](mapi-constants.md)

