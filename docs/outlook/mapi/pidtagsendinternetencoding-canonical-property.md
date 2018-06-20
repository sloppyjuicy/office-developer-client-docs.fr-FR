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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b6814df2b28961be7e8c07a2d19932988605dc87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786761"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="45018-103">Propriété canonique PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="45018-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="45018-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45018-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45018-105">Contient un masque binaire composé des préférences de codage.</span><span class="sxs-lookup"><span data-stu-id="45018-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45018-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="45018-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45018-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="45018-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="45018-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="45018-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45018-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="45018-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="45018-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="45018-110">Data type:</span></span>  <br/> |<span data-ttu-id="45018-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45018-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45018-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="45018-112">Area:</span></span>  <br/> |<span data-ttu-id="45018-113">Address</span><span class="sxs-lookup"><span data-stu-id="45018-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45018-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="45018-114">Remarks</span></span>

<span data-ttu-id="45018-115">Définir cette propriété pour indiquer les options de codage utilisées.</span><span class="sxs-lookup"><span data-stu-id="45018-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="45018-116">Cette propriété contient les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="45018-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="45018-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="45018-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="45018-118">Coder le texte du message dans le code HTML.</span><span class="sxs-lookup"><span data-stu-id="45018-118">Encode the message text in HTML.</span></span> <span data-ttu-id="45018-119">Cet indicateur est ignoré à moins que l’indicateur ENCODING_MIME est défini.</span><span class="sxs-lookup"><span data-stu-id="45018-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="45018-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="45018-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="45018-121">Coder le texte du message à l’aide de texte et HTML en tant que solutions à parties multiples Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="45018-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="45018-122">Cet indicateur est ignoré à moins que l’indicateur ENCODING_MIME est défini.</span><span class="sxs-lookup"><span data-stu-id="45018-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="45018-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="45018-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="45018-124">Coder le message à l’aide de MIME.</span><span class="sxs-lookup"><span data-stu-id="45018-124">Encode the message using MIME.</span></span> <span data-ttu-id="45018-125">Si cet indicateur n’est pas défini, MAPI encode le texte du message en texte brut et les pièces jointes dans UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="45018-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="45018-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="45018-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="45018-127">Utilisez les autres indicateurs dans ce masque de bits pour déterminer le type de codage.</span><span class="sxs-lookup"><span data-stu-id="45018-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="45018-128">Si cet indicateur n’est pas défini, MAPI laisse au système de messagerie pour prendre des décisions de codage.</span><span class="sxs-lookup"><span data-stu-id="45018-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="45018-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="45018-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="45018-130">Coder les pièces jointes de Macintosh en mode double Apple.</span><span class="sxs-lookup"><span data-stu-id="45018-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="45018-131">Cet indicateur est ignoré à moins que l’indicateur ENCODING_MIME est défini.</span><span class="sxs-lookup"><span data-stu-id="45018-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="45018-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="45018-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="45018-133">Coder les pièces jointes de Macintosh en mode unique Apple.</span><span class="sxs-lookup"><span data-stu-id="45018-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="45018-134">Cet indicateur est ignoré à moins que l’indicateur ENCODING_MIME est défini.</span><span class="sxs-lookup"><span data-stu-id="45018-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="45018-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="45018-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="45018-136">Coder les pièces jointes de Macintosh dans UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="45018-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="45018-137">Si l’indicateur ENCODING_MIME est défini, cet indicateur est ignoré et codage BinHex est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="45018-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="45018-138">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="45018-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45018-139">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="45018-139">Protocol specifications</span></span>

<span data-ttu-id="45018-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45018-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45018-141">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="45018-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45018-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45018-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45018-143">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="45018-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="45018-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45018-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45018-145">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="45018-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="45018-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45018-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45018-147">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="45018-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="45018-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45018-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45018-149">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="45018-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45018-150">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="45018-150">Header files</span></span>

<span data-ttu-id="45018-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45018-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="45018-152">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="45018-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="45018-153">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="45018-153">Mapitags.h</span></span>
  
> <span data-ttu-id="45018-154">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="45018-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45018-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45018-155">See also</span></span>



[<span data-ttu-id="45018-156">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="45018-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45018-157">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="45018-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45018-158">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="45018-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45018-159">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="45018-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

