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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c93d850551e766e97292d5417c3be5577f557af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786628"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="1c671-103">Propriété canonique PidTagRtfCompressed</span><span class="sxs-lookup"><span data-stu-id="1c671-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="1c671-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c671-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c671-105">Contient la version RTF (RICH Text Format) du texte du message, généralement dans un format compressé.</span><span class="sxs-lookup"><span data-stu-id="1c671-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c671-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1c671-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c671-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="1c671-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="1c671-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1c671-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c671-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="1c671-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="1c671-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1c671-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c671-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c671-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1c671-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="1c671-112">Area:</span></span>  <br/> |<span data-ttu-id="1c671-113">Courier électronique</span><span class="sxs-lookup"><span data-stu-id="1c671-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c671-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c671-114">Remarks</span></span>

<span data-ttu-id="1c671-115">Cette propriété contient le texte du message même que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), mais au format RTF.</span><span class="sxs-lookup"><span data-stu-id="1c671-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="1c671-116">Texte du message au format RTF est généralement stockée dans format compressé.</span><span class="sxs-lookup"><span data-stu-id="1c671-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="1c671-117">Toutefois, certains systèmes ne pas condenser texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="1c671-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="1c671-118">Pour prendre en compte les, MAPI fournit la valeur de dwMagicUncompressedRTF pour un en-tête de flux identifier les RTF décompressé et l’indicateur **STORE_UNCOMPRESSED_RTF** dans **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour le message magasin pour indiquer qu’elle peut stocker RTF décompressé.</span><span class="sxs-lookup"><span data-stu-id="1c671-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="1c671-119">Pour obtenir le contenu de cette propriété, appelez **OpenProperty**, puis appelez [WrapCompressedRTFStream](wrapcompressedrtfstream.md) avec l’indicateur **MAPI_READ** .</span><span class="sxs-lookup"><span data-stu-id="1c671-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="1c671-120">Pour écrire dans cette propriété, ouvrez-le avec les indicateurs **** n’et **MAPI_CREATE** .</span><span class="sxs-lookup"><span data-stu-id="1c671-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="1c671-121">Cela garantit que les nouvelles données remplacent complètement toutes les anciennes données et que les écritures sont exécutées en utilisant le nombre minimal de mises à jour de la banque.</span><span class="sxs-lookup"><span data-stu-id="1c671-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="1c671-122">Banques de messages qui prennent en charge le format RTF ignorent toutes les modifications dans l’espace blanc dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="1c671-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="1c671-123">Lorsque **PR_BODY** est stockée pour la première fois, la banque de messages également génère et stocke cette propriété.</span><span class="sxs-lookup"><span data-stu-id="1c671-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="1c671-124">Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée par la suite et **PR_BODY** a été modifié, la banque de messages appelle la fonction de [RTFSync](rtfsync.md) pour assurer la synchronisation avec la version RTF.</span><span class="sxs-lookup"><span data-stu-id="1c671-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="1c671-125">Si seule l’espace blanc a été modifié, les propriétés restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="1c671-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="1c671-126">Ainsi, n’importe quel format RTF important mise en forme lorsque le message transite par non RTF-prenant en charge les clients et les systèmes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1c671-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1c671-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1c671-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c671-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1c671-128">Protocol specifications</span></span>

<span data-ttu-id="1c671-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c671-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c671-130">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="1c671-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c671-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c671-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c671-132">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1c671-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="1c671-133">[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c671-133">[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c671-134">Code et décode un flux compressé dans le corps de message RTF.</span><span class="sxs-lookup"><span data-stu-id="1c671-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="1c671-135">[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c671-135">[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c671-136">Encapsule des formats de contenu supplémentaires (tels que HTML) dans la propriété body RTF des messages et pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="1c671-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c671-137">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1c671-137">Header files</span></span>

<span data-ttu-id="1c671-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c671-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c671-139">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1c671-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c671-140">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1c671-140">Mapitags.h</span></span>
  
> <span data-ttu-id="1c671-141">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1c671-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c671-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c671-142">See also</span></span>



[<span data-ttu-id="1c671-143">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1c671-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c671-144">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1c671-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c671-145">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1c671-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c671-146">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="1c671-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

