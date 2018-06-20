---
title: Propriété canonique PidTagOriginalSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6cf81a5b4c10cb7bff5f03a1b25d11bbaa8ff277
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786348"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="3aaab-103">Propriété canonique PidTagOriginalSubject</span><span class="sxs-lookup"><span data-stu-id="3aaab-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="3aaab-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3aaab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3aaab-105">Contient l’objet du message d’origine pour une utilisation dans un rapport sur le message.</span><span class="sxs-lookup"><span data-stu-id="3aaab-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3aaab-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3aaab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3aaab-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="3aaab-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="3aaab-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3aaab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3aaab-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="3aaab-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="3aaab-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3aaab-110">Data type:</span></span>  <br/> |<span data-ttu-id="3aaab-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3aaab-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3aaab-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="3aaab-112">Area:</span></span>  <br/> |<span data-ttu-id="3aaab-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="3aaab-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3aaab-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3aaab-114">Remarks</span></span>

<span data-ttu-id="3aaab-115">Ces propriétés sont initialement définies pour la même valeur que la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3aaab-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="3aaab-116">Les propriétés de l’objet sont généralement petites chaînes de moins de 256 caractères, et un fournisseur de magasin de message n’est pas tenu prendre en charge l’interface Object Linking and Embedding (OLE) **IStream** sur eux.</span><span class="sxs-lookup"><span data-stu-id="3aaab-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="3aaab-117">Le client doit toujours tentent d’accéder par le biais de l’interface **IMAPIProp** tout d’abord et recourir aux **IStream** que si **MAPI_E_NOT_ENOUGH_MEMORY** est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="3aaab-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3aaab-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3aaab-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3aaab-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3aaab-119">Protocol specifications</span></span>

<span data-ttu-id="3aaab-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3aaab-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3aaab-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="3aaab-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3aaab-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3aaab-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3aaab-123">Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="3aaab-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="3aaab-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3aaab-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3aaab-125">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="3aaab-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3aaab-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3aaab-126">Header files</span></span>

<span data-ttu-id="3aaab-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3aaab-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3aaab-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3aaab-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="3aaab-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3aaab-129">Mapitags.h</span></span>
  
> <span data-ttu-id="3aaab-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3aaab-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3aaab-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aaab-131">See also</span></span>



[<span data-ttu-id="3aaab-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3aaab-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3aaab-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3aaab-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3aaab-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3aaab-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3aaab-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3aaab-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

