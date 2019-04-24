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
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342671"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="d7bc3-103">Propriété canonique PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="d7bc3-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="d7bc3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7bc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7bc3-105">Contient un masque de masque des préférences de codage.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7bc3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d7bc3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7bc3-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="d7bc3-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="d7bc3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d7bc3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7bc3-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="d7bc3-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="d7bc3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d7bc3-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7bc3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d7bc3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d7bc3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d7bc3-112">Area:</span></span>  <br/> |<span data-ttu-id="d7bc3-113">Address</span><span class="sxs-lookup"><span data-stu-id="d7bc3-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7bc3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7bc3-114">Remarks</span></span>

<span data-ttu-id="d7bc3-115">Définissez cette propriété pour indiquer les options d'encodage utilisées.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="d7bc3-116">Cette propriété contient les indicateurs suivants:</span><span class="sxs-lookup"><span data-stu-id="d7bc3-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="d7bc3-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="d7bc3-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="d7bc3-118">Codez le texte du message au format HTML.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-118">Encode the message text in HTML.</span></span> <span data-ttu-id="d7bc3-119">Cet indicateur est ignoré sauf si l'indicateur ENCODING_MIME est défini.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="d7bc3-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="d7bc3-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="d7bc3-121">Codez le texte du message en utilisant du texte et du code HTML en tant que solutions multifonctions MIME (Multipurpose Internet Mail Extensions) en plusieurs parties.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="d7bc3-122">Cet indicateur est ignoré sauf si l'indicateur ENCODING_MIME est défini.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="d7bc3-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="d7bc3-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="d7bc3-124">Codez le message en utilisant MIME.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-124">Encode the message using MIME.</span></span> <span data-ttu-id="d7bc3-125">Si cet indicateur n'est pas défini, MAPI code le texte du message en texte brut et les pièces jointes dans UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="d7bc3-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="d7bc3-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="d7bc3-127">Utilisez les autres indicateurs de ce masque pour déterminer le codage.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="d7bc3-128">Si cet indicateur n'est pas défini, MAPI le laisse au système de messagerie afin de prendre des décisions de codage.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="d7bc3-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="d7bc3-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="d7bc3-130">Coder les pièces jointes Macintosh en mode double de Apple.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="d7bc3-131">Cet indicateur est ignoré sauf si l'indicateur ENCODING_MIME est défini.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="d7bc3-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="d7bc3-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="d7bc3-133">Coder les pièces jointes Macintosh en mode simple Apple.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="d7bc3-134">Cet indicateur est ignoré sauf si l'indicateur ENCODING_MIME est défini.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="d7bc3-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="d7bc3-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="d7bc3-136">Coder les pièces jointes Macintosh dans UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="d7bc3-137">Si l'indicateur ENCODING_MIME est défini, cet indicateur est ignoré et l'encodage BinHex est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="d7bc3-138">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="d7bc3-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7bc3-139">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d7bc3-139">Protocol specifications</span></span>

<span data-ttu-id="d7bc3-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7bc3-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7bc3-141">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7bc3-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7bc3-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7bc3-143">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="d7bc3-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7bc3-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7bc3-145">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="d7bc3-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7bc3-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7bc3-147">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d7bc3-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7bc3-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7bc3-149">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7bc3-150">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="d7bc3-150">Header files</span></span>

<span data-ttu-id="d7bc3-151">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d7bc3-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7bc3-152">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7bc3-153">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d7bc3-153">Mapitags.h</span></span>
  
> <span data-ttu-id="d7bc3-154">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="d7bc3-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7bc3-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7bc3-155">See also</span></span>



[<span data-ttu-id="d7bc3-156">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d7bc3-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7bc3-157">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d7bc3-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7bc3-158">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d7bc3-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7bc3-159">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d7bc3-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

