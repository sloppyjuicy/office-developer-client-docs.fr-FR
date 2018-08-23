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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c88e6789b5b48e946d86a0458674a0fbe6b76356
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575447"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="808c3-103">Propriété canonique PidTagRtfCompressed</span><span class="sxs-lookup"><span data-stu-id="808c3-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="808c3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="808c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="808c3-105">Contient la version RTF (RICH Text Format) du texte du message, généralement dans un format compressé.</span><span class="sxs-lookup"><span data-stu-id="808c3-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="808c3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="808c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="808c3-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="808c3-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="808c3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="808c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="808c3-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="808c3-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="808c3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="808c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="808c3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="808c3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="808c3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="808c3-112">Area:</span></span>  <br/> |<span data-ttu-id="808c3-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="808c3-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="808c3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="808c3-114">Remarks</span></span>

<span data-ttu-id="808c3-115">Cette propriété contient le texte du message même que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), mais au format RTF.</span><span class="sxs-lookup"><span data-stu-id="808c3-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="808c3-116">Texte du message au format RTF est généralement stockée dans format compressé.</span><span class="sxs-lookup"><span data-stu-id="808c3-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="808c3-117">Toutefois, certains systèmes ne pas condenser texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="808c3-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="808c3-118">Pour prendre en compte les, MAPI fournit la valeur de dwMagicUncompressedRTF pour un en-tête de flux identifier les RTF décompressé et l’indicateur **STORE_UNCOMPRESSED_RTF** dans **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour le message magasin pour indiquer qu’elle peut stocker RTF décompressé.</span><span class="sxs-lookup"><span data-stu-id="808c3-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="808c3-119">Pour obtenir le contenu de cette propriété, appelez **OpenProperty**, puis appelez [WrapCompressedRTFStream](wrapcompressedrtfstream.md) avec l’indicateur **MAPI_READ** .</span><span class="sxs-lookup"><span data-stu-id="808c3-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="808c3-120">Pour écrire dans cette propriété, ouvrez-le avec les indicateurs **** n’et **MAPI_CREATE** .</span><span class="sxs-lookup"><span data-stu-id="808c3-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="808c3-121">Cela garantit que les nouvelles données remplacent complètement toutes les anciennes données et que les écritures sont exécutées en utilisant le nombre minimal de mises à jour de la banque.</span><span class="sxs-lookup"><span data-stu-id="808c3-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="808c3-122">Banques de messages qui prennent en charge le format RTF ignorent toutes les modifications dans l’espace blanc dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="808c3-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="808c3-123">Lorsque **PR_BODY** est stockée pour la première fois, la banque de messages également génère et stocke cette propriété.</span><span class="sxs-lookup"><span data-stu-id="808c3-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="808c3-124">Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée par la suite et **PR_BODY** a été modifié, la banque de messages appelle la fonction de [RTFSync](rtfsync.md) pour assurer la synchronisation avec la version RTF.</span><span class="sxs-lookup"><span data-stu-id="808c3-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="808c3-125">Si seule l’espace blanc a été modifié, les propriétés restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="808c3-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="808c3-126">Ainsi, n’importe quel format RTF important mise en forme lorsque le message transite par non RTF-prenant en charge les clients et les systèmes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="808c3-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="808c3-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="808c3-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="808c3-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="808c3-128">Protocol specifications</span></span>

<span data-ttu-id="808c3-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="808c3-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="808c3-130">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="808c3-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="808c3-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="808c3-131">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="808c3-132">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="808c3-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="808c3-133">[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="808c3-133">[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="808c3-134">Code et décode un flux compressé dans le corps de message RTF.</span><span class="sxs-lookup"><span data-stu-id="808c3-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="808c3-135">[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="808c3-135">[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="808c3-136">Encapsule des formats de contenu supplémentaires (tels que HTML) dans la propriété body RTF des messages et pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="808c3-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="808c3-137">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="808c3-137">Header files</span></span>

<span data-ttu-id="808c3-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="808c3-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="808c3-139">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="808c3-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="808c3-140">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="808c3-140">Mapitags.h</span></span>
  
> <span data-ttu-id="808c3-141">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="808c3-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="808c3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="808c3-142">See also</span></span>



[<span data-ttu-id="808c3-143">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="808c3-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="808c3-144">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="808c3-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="808c3-145">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="808c3-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="808c3-146">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="808c3-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

