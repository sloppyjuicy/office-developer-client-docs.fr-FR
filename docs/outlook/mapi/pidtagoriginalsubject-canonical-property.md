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
ms.openlocfilehash: de957c33165cc96eec82bf95c8f292c5b323676a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331142"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="de64e-103">Propriété canonique PidTagOriginalSubject</span><span class="sxs-lookup"><span data-stu-id="de64e-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="de64e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de64e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de64e-105">Contient l'objet d'un message d'origine à utiliser dans un rapport sur le message.</span><span class="sxs-lookup"><span data-stu-id="de64e-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de64e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="de64e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de64e-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="de64e-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="de64e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="de64e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de64e-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="de64e-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="de64e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="de64e-110">Data type:</span></span>  <br/> |<span data-ttu-id="de64e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="de64e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="de64e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="de64e-112">Area:</span></span>  <br/> |<span data-ttu-id="de64e-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="de64e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de64e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="de64e-114">Remarks</span></span>

<span data-ttu-id="de64e-115">Ces propriétés sont initialement définies sur la même valeur que la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="de64e-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="de64e-116">Les propriétés Subject sont généralement des petites chaînes de moins de 256 caractères et un fournisseur de banque de messages n'est pas tenu de prendre en charge l'interface OLE (Object Linking and Embedding) **IStream** .</span><span class="sxs-lookup"><span data-stu-id="de64e-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="de64e-117">Le client doit toujours tenter d'accéder d'abord à travers l'interface **IMAPIProp** et ne recourir à **IStream** que si **MAPI_E_NOT_ENOUGH_MEMORY** est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="de64e-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="de64e-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="de64e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de64e-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="de64e-119">Protocol specifications</span></span>

<span data-ttu-id="de64e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de64e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de64e-121">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="de64e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de64e-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de64e-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de64e-123">Gère la synchronisation des données d'objet de messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="de64e-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="de64e-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de64e-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de64e-125">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="de64e-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de64e-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="de64e-126">Header files</span></span>

<span data-ttu-id="de64e-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="de64e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="de64e-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="de64e-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="de64e-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="de64e-129">Mapitags.h</span></span>
  
> <span data-ttu-id="de64e-130">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="de64e-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de64e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de64e-131">See also</span></span>



[<span data-ttu-id="de64e-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="de64e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de64e-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="de64e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de64e-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="de64e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de64e-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="de64e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

