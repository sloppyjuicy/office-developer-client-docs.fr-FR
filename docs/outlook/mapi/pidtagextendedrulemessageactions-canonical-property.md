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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316337"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="aabf1-103">Propriété canonique PidTagExtendedRuleMessageActions</span><span class="sxs-lookup"><span data-stu-id="aabf1-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="aabf1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aabf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aabf1-105">Contient des informations supplémentaires sur les propriétés nommées utilisées dans un message FAI (Folder Associated Information).</span><span class="sxs-lookup"><span data-stu-id="aabf1-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aabf1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="aabf1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aabf1-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="aabf1-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="aabf1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="aabf1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aabf1-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="aabf1-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="aabf1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="aabf1-110">Data type:</span></span>  <br/> |<span data-ttu-id="aabf1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aabf1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="aabf1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="aabf1-112">Area:</span></span>  <br/> |<span data-ttu-id="aabf1-113">Règles</span><span class="sxs-lookup"><span data-stu-id="aabf1-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aabf1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="aabf1-114">Remarks</span></span>

<span data-ttu-id="aabf1-115">Cette propriété doit être définie sur un message FAI.</span><span class="sxs-lookup"><span data-stu-id="aabf1-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="aabf1-116">Cette propriété a le même objectif que **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), mais contient des informations supplémentaires sur la version de la règle et les propriétés nommées stockées dans l’action de règle, ainsi que des informations sur les actions à effectuer par cette règle.</span><span class="sxs-lookup"><span data-stu-id="aabf1-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="aabf1-117">Toutes les valeurs de chaîne contenues dans n’importe quelle partie de la mémoire tampon d’action utilisée pour contenir des actions doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="aabf1-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="aabf1-118">Pour plus d’informations sur le format de cette propriété binaire, voir [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aabf1-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aabf1-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="aabf1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aabf1-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="aabf1-120">Protocol specifications</span></span>

<span data-ttu-id="aabf1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aabf1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aabf1-122">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="aabf1-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="aabf1-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aabf1-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aabf1-124">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="aabf1-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aabf1-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="aabf1-125">Header files</span></span>

<span data-ttu-id="aabf1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aabf1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="aabf1-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="aabf1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="aabf1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aabf1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="aabf1-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="aabf1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aabf1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aabf1-130">See also</span></span>



[<span data-ttu-id="aabf1-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="aabf1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aabf1-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="aabf1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aabf1-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="aabf1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aabf1-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="aabf1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

