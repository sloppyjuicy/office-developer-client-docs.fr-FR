---
title: Propriété canonique PidLidReferenceEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReferenceEntryId
api_type:
- COM
ms.assetid: 42e7c3ac-1a04-4e3f-bf99-ef3f8fc45892
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f5bad81f6317522430b92324ff497754376e0f19
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393760"
---
# <a name="pidlidreferenceentryid-canonical-property"></a><span data-ttu-id="56289-103">Propriété canonique PidLidReferenceEntryId</span><span class="sxs-lookup"><span data-stu-id="56289-103">PidLidReferenceEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="56289-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56289-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56289-105">Spécifie la référence [ENTRYID](entryid.md) pour le contact.</span><span class="sxs-lookup"><span data-stu-id="56289-105">Specifies the reference [ENTRYID](entryid.md) for the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56289-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="56289-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56289-107">dispidReferenceEID</span><span class="sxs-lookup"><span data-stu-id="56289-107">dispidReferenceEID</span></span>  <br/> |
|<span data-ttu-id="56289-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="56289-108">Property set:</span></span>  <br/> |<span data-ttu-id="56289-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="56289-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="56289-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="56289-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="56289-111">0x000085BD</span><span class="sxs-lookup"><span data-stu-id="56289-111">0x000085BD</span></span>  <br/> |
|<span data-ttu-id="56289-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="56289-112">Data type:</span></span>  <br/> |<span data-ttu-id="56289-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="56289-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="56289-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="56289-114">Area:</span></span>  <br/> |<span data-ttu-id="56289-115">Contact</span><span class="sxs-lookup"><span data-stu-id="56289-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56289-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="56289-116">Remarks</span></span>

<span data-ttu-id="56289-117">Le cas échéant, cette propriété doit être égale à la valeur de **propriété EntryId** du contact.</span><span class="sxs-lookup"><span data-stu-id="56289-117">If present, this property should be equal to the value of the **EntryId** of the contact.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="56289-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="56289-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56289-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="56289-119">Protocol specifications</span></span>

<span data-ttu-id="56289-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56289-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56289-121">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="56289-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56289-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56289-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56289-123">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="56289-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56289-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="56289-124">Header files</span></span>

<span data-ttu-id="56289-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56289-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="56289-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="56289-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56289-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56289-127">See also</span></span>



[<span data-ttu-id="56289-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="56289-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56289-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="56289-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56289-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="56289-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56289-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="56289-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

