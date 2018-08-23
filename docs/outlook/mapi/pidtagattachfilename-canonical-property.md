---
title: Propriété canonique PidTagAttachFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c5354618383a97b362348b14aea174d6f2266d6c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583280"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="8da1c-103">Propriété canonique PidTagAttachFilename</span><span class="sxs-lookup"><span data-stu-id="8da1c-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="8da1c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8da1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8da1c-105">Contient le nom de fichier de base et l’extension à l’exclusion du chemin d’accès d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="8da1c-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8da1c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8da1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8da1c-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="8da1c-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="8da1c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8da1c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8da1c-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="8da1c-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="8da1c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8da1c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8da1c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8da1c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8da1c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8da1c-112">Area:</span></span>  <br/> |<span data-ttu-id="8da1c-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="8da1c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8da1c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8da1c-114">Remarks</span></span>

<span data-ttu-id="8da1c-115">Il est recommandé que les objets attachment exposent ces propriétés qui s’appliquent aux valeurs de la **PR_ATTACH_METHOD** **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**et **ATTACH_BY_REF_ONLY** Propriété ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8da1c-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="8da1c-116">**PR_ATTACH_FILENAME** et propriétés associées sont requis quand un de ces valeurs est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8da1c-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="8da1c-117">Ces propriétés peuvent être utilisées comme nom de fichier suggéré pour enregistrer la pièce jointe et leur fournir l’extension de nom de fichier si la propriété **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) n’est pas fournie.</span><span class="sxs-lookup"><span data-stu-id="8da1c-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="8da1c-118">Le nom de fichier est limité à huit caractères et une extension de trois caractères.</span><span class="sxs-lookup"><span data-stu-id="8da1c-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="8da1c-119">Pour une plate-forme qui prend en charge les noms de fichiers longs, définissez cette propriété et la propriété **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8da1c-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="8da1c-120">MAPI ne fonctionne qu’avec les noms de fichiers et autres chaînes passé, dans le jeu de caractères National Institute ANSI (American Standards).</span><span class="sxs-lookup"><span data-stu-id="8da1c-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="8da1c-121">Les applications clientes qui utilisent des noms de fichiers dans un jeu de caractères OEM (OEM) doivent les convertir au format ANSI avant l’appel de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8da1c-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8da1c-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8da1c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8da1c-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8da1c-123">Protocol specifications</span></span>

<span data-ttu-id="8da1c-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8da1c-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8da1c-125">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="8da1c-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8da1c-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8da1c-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8da1c-127">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="8da1c-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="8da1c-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8da1c-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8da1c-129">Spécifie les propriétés des messages codés géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="8da1c-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="8da1c-130">[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8da1c-130">[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8da1c-131">Spécifie S/MIME signés et chiffrés des propriétés de message.</span><span class="sxs-lookup"><span data-stu-id="8da1c-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="8da1c-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8da1c-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8da1c-133">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="8da1c-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8da1c-134">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8da1c-134">Header files</span></span>

<span data-ttu-id="8da1c-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8da1c-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="8da1c-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8da1c-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="8da1c-137">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8da1c-137">Mapitags.h</span></span>
  
> <span data-ttu-id="8da1c-138">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8da1c-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8da1c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8da1c-139">See also</span></span>



[<span data-ttu-id="8da1c-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8da1c-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8da1c-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8da1c-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8da1c-142">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8da1c-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8da1c-143">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8da1c-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

