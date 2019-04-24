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
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315385"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="6e5dd-103">Propriété canonique PidLidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="6e5dd-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="6e5dd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e5dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e5dd-105">Vérifie si la valeur de la propriété **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) a été définie par un agent qui savait la valeur de la propriété **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6e5dd-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e5dd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6e5dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e5dd-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="6e5dd-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="6e5dd-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="6e5dd-108">Property set:</span></span>  <br/> |<span data-ttu-id="6e5dd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6e5dd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6e5dd-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="6e5dd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6e5dd-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="6e5dd-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="6e5dd-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6e5dd-112">Data type:</span></span>  <br/> |<span data-ttu-id="6e5dd-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6e5dd-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6e5dd-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6e5dd-114">Area:</span></span>  <br/> |<span data-ttu-id="6e5dd-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="6e5dd-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e5dd-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e5dd-116">Remarks</span></span>

<span data-ttu-id="6e5dd-117">Pour les objets qui ne sont pas des expéditeurs (messages reçus et objets autres que des objets de messagerie), les clients doivent définir cette valeur sur la valeur de **PR_MESSAGE_DELIVERY_TIME** lors de la modification de **dispidRequest**.</span><span class="sxs-lookup"><span data-stu-id="6e5dd-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="6e5dd-118">Étant donné que la valeur de **PR_MESSAGE_DELIVERY_TIME** ne peut pas être prévisible par l'expéditeur, si la valeur de cette propriété est égale à la valeur de **PR_MESSAGE_DELIVERY_TIME**, il est raisonnablement certain que la valeur de **dispidRequest** n'a pas proviennent de l'expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="6e5dd-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="6e5dd-119">Un client peut décider comment présenter la valeur de **dispidRequest** à l'utilisateur final en fonction du résultat de cette comparaison conformément à la stratégie de sécurité spécifique du client.</span><span class="sxs-lookup"><span data-stu-id="6e5dd-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="6e5dd-120">Si la valeur de **dispidRequest** est ignorée en raison de la présence d'une valeur pour **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), cette propriété doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="6e5dd-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e5dd-121">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="6e5dd-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e5dd-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6e5dd-122">Protocol specifications</span></span>

<span data-ttu-id="6e5dd-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e5dd-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e5dd-124">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="6e5dd-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e5dd-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e5dd-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e5dd-126">Spécifie les propriétés et les opérations relatives au marquage.</span><span class="sxs-lookup"><span data-stu-id="6e5dd-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e5dd-127">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="6e5dd-127">Header files</span></span>

<span data-ttu-id="6e5dd-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6e5dd-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e5dd-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6e5dd-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e5dd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e5dd-130">See also</span></span>



[<span data-ttu-id="6e5dd-131">Propriété canonique PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="6e5dd-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="6e5dd-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6e5dd-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e5dd-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6e5dd-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e5dd-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6e5dd-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e5dd-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6e5dd-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

