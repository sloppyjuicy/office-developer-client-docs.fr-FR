---
title: IConverterSessionSetCharSet
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
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336658"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="3b65d-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="3b65d-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="3b65d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b65d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b65d-105">Spécifie un jeu de caractères facultatif que le convertisseur MAPI en MIME utilise lors de la conversion d’un message MAPI en flux MIME.</span><span class="sxs-lookup"><span data-stu-id="3b65d-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="3b65d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3b65d-106">Parameters</span></span>

 <span data-ttu-id="3b65d-107">_fApply_</span><span class="sxs-lookup"><span data-stu-id="3b65d-107">_fApply_</span></span>
  
> <span data-ttu-id="3b65d-108">[in] Indique s’il faut utiliser un jeu de caractères spécifique pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="3b65d-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="3b65d-109">Définissez ce paramètre sur **true** pour appliquer le jeu de caractères dans les conversions suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b65d-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="3b65d-110">Définissez ce paramètre sur **false** si vous ne souhaitez plus appliquer de jeu de caractères spécifique et revenir aux valeurs par défaut pour les messages suivants.</span><span class="sxs-lookup"><span data-stu-id="3b65d-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="3b65d-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="3b65d-111">_hcharset_</span></span>
  
> <span data-ttu-id="3b65d-112">[in] Handle vers un jeu de caractères défini dans mimeole.h de Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="3b65d-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="3b65d-113">Spécifiez **null** pour spécifier que vous ne souhaitez pas appliquer de jeu de caractères spécifique.</span><span class="sxs-lookup"><span data-stu-id="3b65d-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="3b65d-114">Pour les valeurs **non null,** utilisez une fonction telle que [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) pour obtenir un handle vers le jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="3b65d-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="3b65d-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="3b65d-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="3b65d-116">[in] Indique comment appliquer un jeu de caractères pour convertir un message, tel que défini dans mimeole.h de Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="3b65d-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b65d-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3b65d-117">Return value</span></span>

<span data-ttu-id="3b65d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b65d-118">S_OK</span></span>
  
> <span data-ttu-id="3b65d-119">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="3b65d-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="3b65d-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3b65d-120">MFCMAPI reference</span></span>

<span data-ttu-id="3b65d-121">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3b65d-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3b65d-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3b65d-122">**File**</span></span>|<span data-ttu-id="3b65d-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3b65d-123">**Function**</span></span>|<span data-ttu-id="3b65d-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3b65d-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b65d-125">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="3b65d-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3b65d-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="3b65d-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="3b65d-127">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.</span><span class="sxs-lookup"><span data-stu-id="3b65d-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="3b65d-128">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="3b65d-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3b65d-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="3b65d-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="3b65d-130">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.</span><span class="sxs-lookup"><span data-stu-id="3b65d-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b65d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b65d-131">See also</span></span>



[<span data-ttu-id="3b65d-132">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b65d-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="3b65d-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="3b65d-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="3b65d-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="3b65d-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="3b65d-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="3b65d-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="3b65d-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="3b65d-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="3b65d-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="3b65d-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="3b65d-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="3b65d-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

