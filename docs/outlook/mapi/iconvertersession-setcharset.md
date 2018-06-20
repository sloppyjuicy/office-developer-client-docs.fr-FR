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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 032f071e18af3a89a2850cf2bd1e141f34bc86d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783661"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="79e78-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="79e78-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="79e78-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79e78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79e78-105">Spécifie qu'un caractère facultatif configurer que l’interface MAPI à MIME convertisseur utiliser lors de la conversion d’un message MAPI à un flux de données MIME.</span><span class="sxs-lookup"><span data-stu-id="79e78-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="79e78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79e78-106">Parameters</span></span>

 <span data-ttu-id="79e78-107">_fApply_</span><span class="sxs-lookup"><span data-stu-id="79e78-107">_fApply_</span></span>
  
> <span data-ttu-id="79e78-108">[in] Indique s’il faut utiliser un caractère spécifique défini pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="79e78-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="79e78-109">Définissez ce paramètre sur **true** pour appliquer le jeu de caractères dans les conversions suivantes.</span><span class="sxs-lookup"><span data-stu-id="79e78-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="79e78-110">Définissez ce paramètre sur **false** si vous ne souhaitez plus appliquer n’importe quel jeu de caractères spécifique et revenir à la valeur par défaut pour les messages suivants.</span><span class="sxs-lookup"><span data-stu-id="79e78-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="79e78-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="79e78-111">_hcharset_</span></span>
  
> <span data-ttu-id="79e78-112">[in] Handle vers un jeu défini dans mimeole.h de Windows Mail de caractères.</span><span class="sxs-lookup"><span data-stu-id="79e78-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="79e78-113">Spécifiez **null** pour spécifier que vous ne souhaitez pas appliquer n’importe quel jeu de caractères spécifique.</span><span class="sxs-lookup"><span data-stu-id="79e78-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="79e78-114">Pour des valeurs non - **null** , utilisez la fonction telles que [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) pour obtenir un handle vers le jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="79e78-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="79e78-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="79e78-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="79e78-116">[in] Indique comment appliquer un jeu de caractères à convertir un message, comme défini dans mimeole.h de Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="79e78-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79e78-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="79e78-117">Return value</span></span>

<span data-ttu-id="79e78-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="79e78-118">S_OK</span></span>
  
> <span data-ttu-id="79e78-119">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="79e78-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="79e78-120">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="79e78-120">MFCMAPI reference</span></span>

<span data-ttu-id="79e78-121">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="79e78-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="79e78-122">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="79e78-122">**File**</span></span>|<span data-ttu-id="79e78-123">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="79e78-123">**Function**</span></span>|<span data-ttu-id="79e78-124">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="79e78-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79e78-125">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="79e78-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="79e78-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="79e78-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="79e78-127">MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.</span><span class="sxs-lookup"><span data-stu-id="79e78-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="79e78-128">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="79e78-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="79e78-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="79e78-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="79e78-130">MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.</span><span class="sxs-lookup"><span data-stu-id="79e78-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79e78-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79e78-131">See also</span></span>



[<span data-ttu-id="79e78-132">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79e78-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="79e78-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="79e78-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="79e78-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="79e78-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="79e78-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="79e78-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="79e78-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="79e78-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="79e78-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="79e78-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="79e78-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="79e78-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

