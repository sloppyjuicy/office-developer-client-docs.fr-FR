---
title: Propriété canonique PidTagStoreRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4598ca5e654308f7701b1dd66adb227599773b7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786855"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="1eb8b-103">Propriété canonique PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="1eb8b-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="1eb8b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1eb8b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1eb8b-105">Contient l’identificateur unique comparable binaire (clé d’enregistrement) de la banque de messages dans lequel réside un objet.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1eb8b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1eb8b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1eb8b-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="1eb8b-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="1eb8b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1eb8b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1eb8b-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="1eb8b-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="1eb8b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1eb8b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1eb8b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1eb8b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1eb8b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="1eb8b-112">Area:</span></span>  <br/> |<span data-ttu-id="1eb8b-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="1eb8b-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1eb8b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1eb8b-114">Remarks</span></span>

<span data-ttu-id="1eb8b-115">Pour une banque de messages, cette propriété est identique à la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) de la banque.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="1eb8b-116">La relation entre cette propriété et la **PR_RECORD_KEY** est la même que la relation entre **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1eb8b-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1eb8b-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1eb8b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1eb8b-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1eb8b-118">Protocol specifications</span></span>

<span data-ttu-id="1eb8b-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1eb8b-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1eb8b-120">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="1eb8b-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1eb8b-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1eb8b-122">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1eb8b-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1eb8b-123">Header files</span></span>

<span data-ttu-id="1eb8b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1eb8b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="1eb8b-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="1eb8b-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1eb8b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="1eb8b-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1eb8b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eb8b-128">See also</span></span>



[<span data-ttu-id="1eb8b-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1eb8b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1eb8b-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1eb8b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1eb8b-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1eb8b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1eb8b-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="1eb8b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

