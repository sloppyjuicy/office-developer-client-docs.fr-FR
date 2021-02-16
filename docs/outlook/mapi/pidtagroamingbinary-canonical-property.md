---
title: Propriété canonique PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359562"
---
# <a name="pidtagroamingbinary-canonical-property"></a><span data-ttu-id="8d262-103">Propriété canonique PidTagRoamingBinary</span><span class="sxs-lookup"><span data-stu-id="8d262-103">PidTagRoamingBinary Canonical Property</span></span>

  
  
<span data-ttu-id="8d262-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d262-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d262-105">Contient un flux de message associé à une sous-classe de la **classeIPM.Config'uration.**</span><span class="sxs-lookup"><span data-stu-id="8d262-105">Contains a message stream associated with a subclass of the **IPM.Configuration** class.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d262-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8d262-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d262-107">PR_ROAMING_BINARYSTREAM</span><span class="sxs-lookup"><span data-stu-id="8d262-107">PR_ROAMING_BINARYSTREAM</span></span>  <br/> |
|<span data-ttu-id="8d262-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8d262-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d262-109">0x7C09</span><span class="sxs-lookup"><span data-stu-id="8d262-109">0x7C09</span></span>  <br/> |
|<span data-ttu-id="8d262-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8d262-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d262-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8d262-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8d262-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8d262-112">Area:</span></span>  <br/> |<span data-ttu-id="8d262-113">Configuration</span><span class="sxs-lookup"><span data-stu-id="8d262-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d262-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d262-114">Remarks</span></span>

<span data-ttu-id="8d262-115">Cette propriété contient le flux de données associé à un messageIPM.Configmessage de classe de message **d’uration.**</span><span class="sxs-lookup"><span data-stu-id="8d262-115">This property contains the data stream associated with an **IPM.Configuration** message class message.</span></span> <span data-ttu-id="8d262-116">Le format du flux dépend de la classe de message.</span><span class="sxs-lookup"><span data-stu-id="8d262-116">The format of the stream depends on the message class.</span></span> <span data-ttu-id="8d262-117">Par exemple, un message de type classe **IPM.Config'uration. La mise encomplet automatique** serait mise en forme en tant que [flux de mise encomplet automatique.](autocomplete-stream.md)</span><span class="sxs-lookup"><span data-stu-id="8d262-117">For instance, a message of class type **IPM.Configuration.Autocomplete** would be formatted as an [Autocomplete Stream](autocomplete-stream.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d262-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8d262-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d262-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="8d262-119">Protocol specifications</span></span>

<span data-ttu-id="8d262-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d262-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d262-121">Fournit des références aux spécifications Microsoft Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="8d262-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d262-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d262-122">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d262-123">Spécifie l’emplacement et les propriétés des données de configuration du client et du serveur, telles que les listes de catégories partagées et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="8d262-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d262-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8d262-124">Header files</span></span>

<span data-ttu-id="8d262-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d262-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d262-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8d262-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d262-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d262-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8d262-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="8d262-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d262-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d262-129">See also</span></span>



[<span data-ttu-id="8d262-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8d262-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d262-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8d262-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d262-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8d262-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d262-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8d262-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

