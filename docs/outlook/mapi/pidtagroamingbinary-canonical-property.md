---
title: Propriété canonique PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 97650550704ba844f10131f1a3045ebbfaaaefff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786620"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="f06d3-103">Propriété canonique PidTagRoamingBinary</span><span class="sxs-lookup"><span data-stu-id="f06d3-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="f06d3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f06d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f06d3-105">Contient un flux de message associé à une sous-classe de la **IPM. Configuration** classe.</span><span class="sxs-lookup"><span data-stu-id="f06d3-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f06d3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f06d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f06d3-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="f06d3-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="f06d3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f06d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f06d3-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="f06d3-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="f06d3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f06d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="f06d3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f06d3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f06d3-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="f06d3-112">Area:</span></span>  <br/> |<span data-ttu-id="f06d3-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="f06d3-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f06d3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f06d3-114">Remarks</span></span>

<span data-ttu-id="f06d3-115">Cette propriété contient le flux de données associé à un **IPM. Configuration** message de classe de message.</span><span class="sxs-lookup"><span data-stu-id="f06d3-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="f06d3-116">Le format de l’objet stream dépend de la classe de message.</span><span class="sxs-lookup"><span data-stu-id="f06d3-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="f06d3-117">Par exemple, un message de type de classe **IPM. Configuration.Autocomplete** doit être mis en forme en tant que [flux de saisie semi-automatique](autocomplete-stream.md).</span><span class="sxs-lookup"><span data-stu-id="f06d3-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f06d3-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f06d3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f06d3-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f06d3-119">Protocol specifications</span></span>

<span data-ttu-id="f06d3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f06d3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f06d3-121">Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f06d3-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f06d3-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f06d3-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f06d3-123">Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="f06d3-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f06d3-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f06d3-124">Header files</span></span>

<span data-ttu-id="f06d3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f06d3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f06d3-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f06d3-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f06d3-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f06d3-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f06d3-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="f06d3-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f06d3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f06d3-129">See also</span></span>



[<span data-ttu-id="f06d3-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f06d3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f06d3-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f06d3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f06d3-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f06d3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f06d3-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="f06d3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

