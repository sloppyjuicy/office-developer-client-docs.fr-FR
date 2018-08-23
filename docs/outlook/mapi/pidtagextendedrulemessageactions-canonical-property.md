---
title: Propriété canonique PidTagExtendedRuleMessageActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9b6af0c7fae85a2ea6cbd53159674fdcd32c642c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592767"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="e3c3c-103">Propriété canonique PidTagExtendedRuleMessageActions</span><span class="sxs-lookup"><span data-stu-id="e3c3c-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="e3c3c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3c3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3c3c-105">Contient des informations supplémentaires sur les propriétés nommées utilisée dans un message de dossier associé informations (FAI).</span><span class="sxs-lookup"><span data-stu-id="e3c3c-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3c3c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e3c3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3c3c-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="e3c3c-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="e3c3c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e3c3c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e3c3c-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="e3c3c-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="e3c3c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e3c3c-110">Data type:</span></span>  <br/> |<span data-ttu-id="e3c3c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e3c3c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e3c3c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e3c3c-112">Area:</span></span>  <br/> |<span data-ttu-id="e3c3c-113">Rules</span><span class="sxs-lookup"><span data-stu-id="e3c3c-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3c3c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3c3c-114">Remarks</span></span>

<span data-ttu-id="e3c3c-115">Cette propriété doit être définie sur un message FAI.</span><span class="sxs-lookup"><span data-stu-id="e3c3c-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="e3c3c-116">Cette propriété remplit la même fonction que **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), mais il contient des informations supplémentaires sur la version de la règle et les propriétés nommées stockées dans l’action de règle, ainsi que des informations sur les actions à effectués par cette règle.</span><span class="sxs-lookup"><span data-stu-id="e3c3c-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="e3c3c-117">Toutes les valeurs de chaîne contenues dans n’importe quelle partie de la mémoire tampon action utilisé pour contenir des actions doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e3c3c-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="e3c3c-118">Pour plus d’informations sur le format de cette propriété binaire, voir [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3c3c-118">For information about the format of this binary property, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e3c3c-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e3c3c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3c3c-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e3c3c-120">Protocol specifications</span></span>

<span data-ttu-id="e3c3c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3c3c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3c3c-122">Fournit des références aux spécifications du protocole Exchange Server connexes...</span><span class="sxs-lookup"><span data-stu-id="e3c3c-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="e3c3c-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3c3c-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3c3c-124">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="e3c3c-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3c3c-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e3c3c-125">Header files</span></span>

<span data-ttu-id="e3c3c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3c3c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3c3c-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e3c3c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3c3c-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e3c3c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e3c3c-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e3c3c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3c3c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3c3c-130">See also</span></span>



[<span data-ttu-id="e3c3c-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e3c3c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3c3c-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e3c3c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3c3c-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e3c3c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3c3c-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e3c3c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

