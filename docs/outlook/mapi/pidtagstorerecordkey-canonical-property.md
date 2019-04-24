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
ms.openlocfilehash: d6f858a9f1d3d4620a86621e3f5ecb4ad4609691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278728"
---
# <a name="pidtagstorerecordkey-canonical-property"></a><span data-ttu-id="632b3-103">Propriété canonique PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="632b3-103">PidTagStoreRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="632b3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="632b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="632b3-105">Contient l'identificateur unique, comparable au format binaire (clé d'enregistrement) de la Banque de messages dans laquelle réside un objet.</span><span class="sxs-lookup"><span data-stu-id="632b3-105">Contains the unique binary-comparable identifier (record key) of the message store in which an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="632b3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="632b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="632b3-107">PR_STORE_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="632b3-107">PR_STORE_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="632b3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="632b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="632b3-109">0x0FFA</span><span class="sxs-lookup"><span data-stu-id="632b3-109">0x0FFA</span></span>  <br/> |
|<span data-ttu-id="632b3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="632b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="632b3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="632b3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="632b3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="632b3-112">Area:</span></span>  <br/> |<span data-ttu-id="632b3-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="632b3-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="632b3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="632b3-114">Remarks</span></span>

<span data-ttu-id="632b3-115">Pour une banque de messages, cette propriété est identique à la propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) de la Banque.</span><span class="sxs-lookup"><span data-stu-id="632b3-115">For a message store, this property is identical to the store's own **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="632b3-116">La relation entre cette propriété et **PR_RECORD_KEY** est identique à la relation entre **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="632b3-116">The relationship between this property and **PR_RECORD_KEY** is the same as the relationship between **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="632b3-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="632b3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="632b3-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="632b3-118">Protocol specifications</span></span>

<span data-ttu-id="632b3-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="632b3-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="632b3-120">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="632b3-120">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="632b3-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="632b3-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="632b3-122">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="632b3-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="632b3-123">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="632b3-123">Header files</span></span>

<span data-ttu-id="632b3-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="632b3-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="632b3-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="632b3-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="632b3-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="632b3-126">Mapitags.h</span></span>
  
> <span data-ttu-id="632b3-127">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="632b3-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="632b3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="632b3-128">See also</span></span>



[<span data-ttu-id="632b3-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="632b3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="632b3-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="632b3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="632b3-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="632b3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="632b3-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="632b3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

