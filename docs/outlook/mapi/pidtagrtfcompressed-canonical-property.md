---
title: Propriété canonique PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357889"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="9d7c2-103">Propriété canonique PidTagRtfCompressed</span><span class="sxs-lookup"><span data-stu-id="9d7c2-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="9d7c2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d7c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d7c2-105">Contient la version RTF (Rich Text Format) du texte du message, généralement sous forme compressée.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d7c2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9d7c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d7c2-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="9d7c2-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="9d7c2-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9d7c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d7c2-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="9d7c2-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="9d7c2-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9d7c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d7c2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d7c2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9d7c2-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9d7c2-112">Area:</span></span>  <br/> |<span data-ttu-id="9d7c2-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="9d7c2-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d7c2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d7c2-114">Remarks</span></span>

<span data-ttu-id="9d7c2-115">Cette propriété contient le même texte de message que **la propriété PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), mais en RTF.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="9d7c2-116">Le texte du message au niveau rtf est normalement stocké sous forme compressée.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="9d7c2-117">Toutefois, certains systèmes ne compressent pas le texte formaté.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="9d7c2-118">Pour les prendre en charge, MAPI fournit la valeur dwMagicUncompressedRTF pour un en-tête de flux afin d’identifier le RTF non compressé et l’indicateur **STORE_UNCOMPRESSED_RTF** dans **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour la magasin de messages afin d’indiquer qu’elle peut stocker le RTF non compressé.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="9d7c2-119">Pour obtenir le contenu de cette propriété, appelez **OpenProperty,** puis appelez [WrapCompressedRTFStream](wrapcompressedrtfstream.md) avec l’MAPI_READ’indicateur. </span><span class="sxs-lookup"><span data-stu-id="9d7c2-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="9d7c2-120">Pour écrire dans cette propriété, ouvrez-la avec MAPI_MODIFY **et** **MAPI_CREATE** indicateurs.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="9d7c2-121">Cela garantit que les nouvelles données remplacent complètement les anciennes données et que les écritures sont effectuées à l’aide du nombre minimal de mises à jour de la boutique.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="9d7c2-122">Les magasins de messages qui la prise en charge rtf ignorent les modifications apportées aux espaces dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="9d7c2-123">Lorsque **PR_BODY** est stocké pour la première fois, la boutique de messages génère et stocke également cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="9d7c2-124">Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée et **que PR_BODY a** été modifié, la boutique de messages appelle la fonction [RTFSync](rtfsync.md) pour garantir la synchronisation avec la version RTF.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="9d7c2-125">Si seuls des espaces ont été modifiés, les propriétés restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="9d7c2-126">Cela permet de conserver toute mise en forme RTF nontrivial lorsque le message passe par des clients et des systèmes de messagerie non RTF.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d7c2-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9d7c2-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d7c2-128">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9d7c2-128">Protocol specifications</span></span>

<span data-ttu-id="9d7c2-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d7c2-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d7c2-130">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d7c2-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d7c2-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d7c2-132">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9d7c2-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d7c2-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d7c2-134">Encode et décode un flux compressé dans les corps des messages RTF.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="9d7c2-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d7c2-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d7c2-136">Encapsule les formats de contenu supplémentaires (par exemple, HTML) dans la propriété rtF body des messages et des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d7c2-137">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9d7c2-137">Header files</span></span>

<span data-ttu-id="9d7c2-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d7c2-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d7c2-139">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d7c2-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d7c2-140">Mapitags.h</span></span>
  
> <span data-ttu-id="9d7c2-141">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="9d7c2-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d7c2-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d7c2-142">See also</span></span>



[<span data-ttu-id="9d7c2-143">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9d7c2-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d7c2-144">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9d7c2-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d7c2-145">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9d7c2-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d7c2-146">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9d7c2-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

