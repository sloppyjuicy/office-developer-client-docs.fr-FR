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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339430"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="a21c0-103">Propriété canonique PidTagPriority</span><span class="sxs-lookup"><span data-stu-id="a21c0-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="a21c0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a21c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a21c0-105">Contient la priorité relative d’un message.</span><span class="sxs-lookup"><span data-stu-id="a21c0-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a21c0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a21c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a21c0-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="a21c0-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="a21c0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a21c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a21c0-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="a21c0-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="a21c0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a21c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="a21c0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a21c0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a21c0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a21c0-112">Area:</span></span>  <br/> |<span data-ttu-id="a21c0-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="a21c0-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a21c0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a21c0-114">Remarks</span></span>

<span data-ttu-id="a21c0-115">Cette propriété et la **propriété PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) ne doivent pas être confondues.</span><span class="sxs-lookup"><span data-stu-id="a21c0-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="a21c0-116">Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse d’envoi du message par le logiciel système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a21c0-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="a21c0-117">Une priorité plus élevée indique généralement un coût plus élevé.</span><span class="sxs-lookup"><span data-stu-id="a21c0-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="a21c0-118">Une importance plus élevée est généralement associée à un affichage différent par l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a21c0-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="a21c0-119">La priorité d’un message de rapport doit être identique à la priorité du message d’origine signalé.</span><span class="sxs-lookup"><span data-stu-id="a21c0-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="a21c0-120">Cette propriété peut avoir exactement l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a21c0-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="a21c0-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="a21c0-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="a21c0-122">Le message n’est pas urgent.</span><span class="sxs-lookup"><span data-stu-id="a21c0-122">The message is not urgent.</span></span>
    
<span data-ttu-id="a21c0-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="a21c0-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="a21c0-124">Le message a une priorité normale.</span><span class="sxs-lookup"><span data-stu-id="a21c0-124">The message has normal priority.</span></span>
    
<span data-ttu-id="a21c0-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="a21c0-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="a21c0-126">Le message est urgent.</span><span class="sxs-lookup"><span data-stu-id="a21c0-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a21c0-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a21c0-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a21c0-128">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a21c0-128">Protocol specifications</span></span>

<span data-ttu-id="a21c0-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a21c0-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a21c0-130">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="a21c0-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a21c0-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a21c0-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a21c0-132">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="a21c0-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a21c0-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a21c0-133">Header files</span></span>

<span data-ttu-id="a21c0-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a21c0-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="a21c0-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a21c0-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="a21c0-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a21c0-136">Mapitags.h</span></span>
  
> <span data-ttu-id="a21c0-137">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="a21c0-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a21c0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a21c0-138">See also</span></span>



[<span data-ttu-id="a21c0-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a21c0-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a21c0-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a21c0-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a21c0-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a21c0-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a21c0-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a21c0-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

