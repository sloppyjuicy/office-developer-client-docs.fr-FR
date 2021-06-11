---
title: Propriété canonique PidTagSendInternetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342671"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="6d735-103">Propriété canonique PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="6d735-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="6d735-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d735-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d735-105">Contient un masque de bits des préférences d’encodage.</span><span class="sxs-lookup"><span data-stu-id="6d735-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d735-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6d735-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d735-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="6d735-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="6d735-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6d735-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d735-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="6d735-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="6d735-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6d735-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d735-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6d735-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6d735-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6d735-112">Area:</span></span>  <br/> |<span data-ttu-id="6d735-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="6d735-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d735-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d735-114">Remarks</span></span>

<span data-ttu-id="6d735-115">Définissez cette propriété pour indiquer les options de codage utilisées.</span><span class="sxs-lookup"><span data-stu-id="6d735-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="6d735-116">Cette propriété contient les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="6d735-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="6d735-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="6d735-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="6d735-118">Encodez le texte du message au format HTML.</span><span class="sxs-lookup"><span data-stu-id="6d735-118">Encode the message text in HTML.</span></span> <span data-ttu-id="6d735-119">Cet indicateur est ignoré, sauf si l’ENCODING_MIME est définie.</span><span class="sxs-lookup"><span data-stu-id="6d735-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="6d735-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="6d735-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="6d735-121">Encodez le texte du message à l’aide de texte et de code HTML en tant qu’alternatives MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="6d735-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="6d735-122">Cet indicateur est ignoré, sauf si l’ENCODING_MIME est définie.</span><span class="sxs-lookup"><span data-stu-id="6d735-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="6d735-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="6d735-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="6d735-124">Encodez le message à l’aide de MIME.</span><span class="sxs-lookup"><span data-stu-id="6d735-124">Encode the message using MIME.</span></span> <span data-ttu-id="6d735-125">Si cet indicateur n’est pas définie, MAPI code le texte du message en texte simple et les pièces jointes dans UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="6d735-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="6d735-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="6d735-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="6d735-127">Utilisez les autres indicateurs de ce masque de bits pour déterminer le codage.</span><span class="sxs-lookup"><span data-stu-id="6d735-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="6d735-128">Si cet indicateur n’est pas définie, MAPI le laisse au système de messagerie pour prendre des décisions d’encodage.</span><span class="sxs-lookup"><span data-stu-id="6d735-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="6d735-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="6d735-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="6d735-130">Codez les pièces jointes Macintosh en mode double Apple.</span><span class="sxs-lookup"><span data-stu-id="6d735-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="6d735-131">Cet indicateur est ignoré, sauf si l’ENCODING_MIME est définie.</span><span class="sxs-lookup"><span data-stu-id="6d735-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="6d735-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="6d735-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="6d735-133">Encodez les pièces jointes Macintosh en mode unique Apple.</span><span class="sxs-lookup"><span data-stu-id="6d735-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="6d735-134">Cet indicateur est ignoré, sauf si l’ENCODING_MIME est définie.</span><span class="sxs-lookup"><span data-stu-id="6d735-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="6d735-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="6d735-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="6d735-136">Codez les pièces jointes Macintosh dans UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="6d735-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="6d735-137">Si l ENCODING_MIME est définie, cet indicateur est ignoré et le codage BinHex est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="6d735-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="6d735-138">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6d735-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d735-139">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6d735-139">Protocol specifications</span></span>

<span data-ttu-id="6d735-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d735-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d735-141">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="6d735-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d735-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d735-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d735-143">Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="6d735-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="6d735-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d735-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d735-145">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="6d735-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6d735-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d735-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d735-147">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6d735-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6d735-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d735-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d735-149">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="6d735-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d735-150">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6d735-150">Header files</span></span>

<span data-ttu-id="6d735-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d735-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d735-152">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6d735-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d735-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d735-153">Mapitags.h</span></span>
  
> <span data-ttu-id="6d735-154">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="6d735-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d735-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d735-155">See also</span></span>



[<span data-ttu-id="6d735-156">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6d735-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d735-157">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6d735-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d735-158">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6d735-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d735-159">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6d735-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

