---
title: Propriété canonique PidTagAttachLongFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339325"
---
# <a name="pidtagattachlongfilename-canonical-property"></a><span data-ttu-id="6cb47-103">Propriété canonique PidTagAttachLongFilename</span><span class="sxs-lookup"><span data-stu-id="6cb47-103">PidTagAttachLongFilename Canonical Property</span></span>

  
  
<span data-ttu-id="6cb47-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cb47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cb47-105">Contient le nom de fichier long et l’extension d’une pièce jointe, à l’exclusion du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="6cb47-105">Contains an attachment's long filename and extension, excluding path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cb47-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6cb47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6cb47-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="6cb47-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="6cb47-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6cb47-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6cb47-109">0x3707</span><span class="sxs-lookup"><span data-stu-id="6cb47-109">0x3707</span></span>  <br/> |
|<span data-ttu-id="6cb47-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6cb47-110">Data type:</span></span>  <br/> |<span data-ttu-id="6cb47-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6cb47-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6cb47-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6cb47-112">Area:</span></span>  <br/> |<span data-ttu-id="6cb47-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="6cb47-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cb47-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6cb47-114">Remarks</span></span>

<span data-ttu-id="6cb47-115">Ces propriétés se rapportent aux valeurs ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE et ATTACH_BY_REF_ONLY de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6cb47-115">These properties pertain to the ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, and ATTACH_BY_REF_ONLY values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="6cb47-116">Les plateformes qui prendre en charge les noms de fichiers longs doivent définir les propriétés **PR_ATTACH_LONG_FILENAME** et **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) lors de l’envoi, et doivent d’abord vérifier **PR_ATTACH_LONG_FILENAME** lors de la réception.</span><span class="sxs-lookup"><span data-stu-id="6cb47-116">Platforms that support long filenames should set both the **PR_ATTACH_LONG_FILENAME** and **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_FILENAME** first when receiving.</span></span> 
  
<span data-ttu-id="6cb47-117">L’application cliente doit définir cette propriété sur un nom de fichier long suggéré à utiliser si l’ordinateur hôte recevant un message prend en charge les noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="6cb47-117">The client application should set this property to a suggested long filename to be used if the host computer receiving a message supports long filenames.</span></span> <span data-ttu-id="6cb47-118">**PR_ATTACH_LONG_FILENAME** peut être utilisé comme nom de fichier pour l’enregistrement de la pièce jointe et pour fournir l’extension de nom de fichier si la propriété **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) n’est pas fournie.</span><span class="sxs-lookup"><span data-stu-id="6cb47-118">**PR_ATTACH_LONG_FILENAME** can be used as a filename for saving the attachment, and to supply the filename extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="6cb47-119">Contrairement au nom de fichier fourni par **PR_ATTACH_FILENAME**, ce nom n’est pas limité à un nom de fichier à huit caractères plus une extension à trois caractères.</span><span class="sxs-lookup"><span data-stu-id="6cb47-119">Unlike the filename provided by **PR_ATTACH_FILENAME**, this name is not restricted to an eight-character filename plus a three-character extension.</span></span> <span data-ttu-id="6cb47-120">Au lieu de cela, il peut y avoir jusqu’à 256 caractères, dont le nom de fichier, l’extension et la période de séparation.</span><span class="sxs-lookup"><span data-stu-id="6cb47-120">Instead, it can be up to 256 characters long, including the filename, extension, and separator period.</span></span> 
  
<span data-ttu-id="6cb47-121">MAPI fonctionne uniquement avec les noms de fichiers dans le jeu de caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="6cb47-121">MAPI works only with filenames in the ANSI character set.</span></span> <span data-ttu-id="6cb47-122">Les applications clientes qui utilisent des noms de fichiers dans un jeu de caractères OEM doivent les convertir en ANSI avant d’appeler MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cb47-122">Client applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6cb47-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6cb47-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6cb47-124">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6cb47-124">Protocol specifications</span></span>

<span data-ttu-id="6cb47-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cb47-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cb47-126">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6cb47-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6cb47-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cb47-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cb47-128">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="6cb47-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6cb47-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cb47-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cb47-130">Spécifie les propriétés des messages codés gérés par des droits.</span><span class="sxs-lookup"><span data-stu-id="6cb47-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="6cb47-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cb47-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cb47-132">Spécifie les propriétés et les opérations autorisées pour la représentation des messages vocaux et de télécopie.</span><span class="sxs-lookup"><span data-stu-id="6cb47-132">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6cb47-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6cb47-133">Header files</span></span>

<span data-ttu-id="6cb47-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6cb47-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="6cb47-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6cb47-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="6cb47-136">Mmapitags.h</span><span class="sxs-lookup"><span data-stu-id="6cb47-136">Mmapitags.h</span></span>
  
> <span data-ttu-id="6cb47-137">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="6cb47-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6cb47-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cb47-138">See also</span></span>



[<span data-ttu-id="6cb47-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6cb47-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6cb47-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6cb47-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6cb47-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6cb47-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6cb47-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6cb47-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

