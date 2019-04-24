---
title: Propriété canonique PidTagAttachPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327229"
---
# <a name="pidtagattachpathname-canonical-property"></a><span data-ttu-id="66111-103">Propriété canonique PidTagAttachPathname</span><span class="sxs-lookup"><span data-stu-id="66111-103">PidTagAttachPathname Canonical Property</span></span>

  
  
<span data-ttu-id="66111-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66111-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66111-105">Contient le chemin d'accès complet et le nom de fichier d'une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="66111-105">Contains an attachment's fully-qualified path and filename.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66111-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="66111-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66111-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="66111-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="66111-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="66111-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66111-109">0x3708</span><span class="sxs-lookup"><span data-stu-id="66111-109">0x3708</span></span>  <br/> |
|<span data-ttu-id="66111-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="66111-110">Data type:</span></span>  <br/> |<span data-ttu-id="66111-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="66111-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="66111-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="66111-112">Area:</span></span>  <br/> |<span data-ttu-id="66111-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="66111-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66111-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="66111-114">Remarks</span></span>

<span data-ttu-id="66111-115">Il est recommandé que les sous-objets des pièces jointes exposent ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="66111-115">It is recommended that attachment subobjects expose these properties.</span></span> <span data-ttu-id="66111-116">Leur définition indique que les données des pièces jointes ne sont pas incluses dans le message, mais qu'elles sont disponibles sur un serveur de fichiers commun.</span><span class="sxs-lookup"><span data-stu-id="66111-116">Setting them indicates that the attachment data is not included with the message but is available on a common file server.</span></span> <span data-ttu-id="66111-117">Ces propriétés sont requises conjointement avec l'un des indicateurs **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) qui indiquent Attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY_REF_ UNIQUEMENT**.</span><span class="sxs-lookup"><span data-stu-id="66111-117">These properties are required in conjunction with any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) flags that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> 
  
<span data-ttu-id="66111-118">Chaque répertoire ou nom de fichier est limité à un nom de huit caractères suivi d'une extension de trois caractères.</span><span class="sxs-lookup"><span data-stu-id="66111-118">Each directory or filename is restricted to an eight-character name plus a three-character extension.</span></span> <span data-ttu-id="66111-119">Le chemin d'accès global est limité à 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="66111-119">The overall path is restricted to 256 characters.</span></span> <span data-ttu-id="66111-120">Pour une plateforme qui prend en charge les noms de fichier longs, définissez ces propriétés et **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="66111-120">For a platform that supports long filenames, set both these properties and **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span></span> 
  
<span data-ttu-id="66111-121">Les applications clientes doivent utiliser une convention d'affectation de noms universelle (UNC) dans la plupart des cas lorsque le fichier est partagé, et doivent utiliser un chemin d'accès absolu lorsque le fichier est local.</span><span class="sxs-lookup"><span data-stu-id="66111-121">Client applications should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="66111-122">MAPI fonctionne uniquement avec les chemins d'accès et les noms de fichier dans le jeu de caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="66111-122">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="66111-123">Les clients qui utilisent des noms de fichiers et des chemins d'accès dans un jeu de caractères OEM doivent les convertir en ANSI avant d'appeler MAPI.</span><span class="sxs-lookup"><span data-stu-id="66111-123">Clients that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="66111-124">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="66111-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66111-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="66111-125">Protocol specifications</span></span>

<span data-ttu-id="66111-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66111-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66111-127">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="66111-127">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="66111-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66111-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66111-129">Spécifie les propriétés des messages codés gérés par des droits.</span><span class="sxs-lookup"><span data-stu-id="66111-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66111-130">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="66111-130">Header files</span></span>

<span data-ttu-id="66111-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="66111-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="66111-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="66111-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="66111-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="66111-133">Mapitags.h</span></span>
  
> <span data-ttu-id="66111-134">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="66111-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66111-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66111-135">See also</span></span>



[<span data-ttu-id="66111-136">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="66111-136">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)
  
[<span data-ttu-id="66111-137">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="66111-137">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)


[<span data-ttu-id="66111-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="66111-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66111-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="66111-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66111-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="66111-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66111-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="66111-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

