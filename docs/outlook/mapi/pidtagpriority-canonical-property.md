---
title: Propriété canonique PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385451"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="4ff01-103">Propriété canonique PidTagPriority</span><span class="sxs-lookup"><span data-stu-id="4ff01-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="4ff01-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ff01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ff01-105">Indique la priorité relative d’un message.</span><span class="sxs-lookup"><span data-stu-id="4ff01-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ff01-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4ff01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ff01-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="4ff01-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="4ff01-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4ff01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ff01-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="4ff01-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="4ff01-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4ff01-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ff01-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4ff01-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4ff01-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4ff01-112">Area:</span></span>  <br/> |<span data-ttu-id="4ff01-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="4ff01-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ff01-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4ff01-114">Remarks</span></span>

<span data-ttu-id="4ff01-115">Cette propriété et la propriété **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) ne doivent pas être confondus.</span><span class="sxs-lookup"><span data-stu-id="4ff01-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="4ff01-116">Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse à laquelle le message doit être envoyé par le logiciel de système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4ff01-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="4ff01-117">Priorité plus élevée indique généralement un coût plus élevé.</span><span class="sxs-lookup"><span data-stu-id="4ff01-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="4ff01-118">Importance supérieure est généralement associée à un autre affichage par l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ff01-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="4ff01-119">La priorité d’un message de rapport doit être identique à la priorité du message d’origine signalée.</span><span class="sxs-lookup"><span data-stu-id="4ff01-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="4ff01-120">Cette propriété peut avoir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ff01-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="4ff01-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="4ff01-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="4ff01-122">Le message n’est pas urgent.</span><span class="sxs-lookup"><span data-stu-id="4ff01-122">The message is not urgent.</span></span>
    
<span data-ttu-id="4ff01-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="4ff01-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="4ff01-124">Le message a une priorité normale.</span><span class="sxs-lookup"><span data-stu-id="4ff01-124">The message has normal priority.</span></span>
    
<span data-ttu-id="4ff01-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="4ff01-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="4ff01-126">Le message est urgent.</span><span class="sxs-lookup"><span data-stu-id="4ff01-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="4ff01-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4ff01-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ff01-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4ff01-128">Protocol specifications</span></span>

<span data-ttu-id="4ff01-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ff01-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ff01-130">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="4ff01-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4ff01-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ff01-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ff01-132">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="4ff01-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ff01-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4ff01-133">Header files</span></span>

<span data-ttu-id="4ff01-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ff01-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ff01-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4ff01-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ff01-136">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4ff01-136">Mapitags.h</span></span>
  
> <span data-ttu-id="4ff01-137">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4ff01-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ff01-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ff01-138">See also</span></span>



[<span data-ttu-id="4ff01-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4ff01-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ff01-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4ff01-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ff01-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4ff01-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ff01-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4ff01-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

