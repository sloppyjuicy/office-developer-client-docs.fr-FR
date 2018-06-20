---
title: Propriété canonique PidLidValidFlagStringProof
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 90f16f33e7e116e124384f9988c0c7dddaad2da5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785536"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="0c104-103">Propriété canonique PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="0c104-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="0c104-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c104-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c104-105">Vérifie si la valeur de la propriété **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) a été définie par un agent qui avait la valeur de la propriété **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0c104-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c104-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0c104-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c104-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="0c104-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="0c104-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="0c104-108">Property set:</span></span>  <br/> |<span data-ttu-id="0c104-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0c104-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0c104-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="0c104-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0c104-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="0c104-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="0c104-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0c104-112">Data type:</span></span>  <br/> |<span data-ttu-id="0c104-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0c104-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="0c104-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="0c104-114">Area:</span></span>  <br/> |<span data-ttu-id="0c104-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="0c104-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c104-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c104-116">Remarks</span></span>

<span data-ttu-id="0c104-117">Sur les objets non expédiable (trafic entrant et objets extérieurs à la messagerie), les clients doivent définir cette valeur à la valeur de **PR_MESSAGE_DELIVERY_TIME** lors de la modification **dispidRequest**.</span><span class="sxs-lookup"><span data-stu-id="0c104-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="0c104-118">Dans la mesure où la valeur de **PR_MESSAGE_DELIVERY_TIME** ne peut pas être prévue par l’expéditeur, si la valeur de cette propriété est égale à la valeur de **PR_MESSAGE_DELIVERY_TIME**, il est certain que la valeur de **dispidRequest** n’a pas issus de l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="0c104-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="0c104-119">Un client peut décider comment présenter la valeur de **dispidRequest** pour l’utilisateur final en fonction du résultat de cette comparaison conformément à la stratégie de sécurité spécifiques du client.</span><span class="sxs-lookup"><span data-stu-id="0c104-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="0c104-120">Si la valeur de **dispidRequest** est ignorée en raison de la présence d’une valeur pour **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), cette propriété doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="0c104-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0c104-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0c104-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c104-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0c104-122">Protocol specifications</span></span>

<span data-ttu-id="0c104-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c104-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c104-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="0c104-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c104-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c104-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c104-126">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="0c104-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c104-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0c104-127">Header files</span></span>

<span data-ttu-id="0c104-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c104-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c104-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0c104-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c104-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c104-130">See also</span></span>



[<span data-ttu-id="0c104-131">Propriété canonique PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="0c104-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="0c104-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0c104-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c104-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0c104-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c104-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0c104-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c104-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="0c104-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

