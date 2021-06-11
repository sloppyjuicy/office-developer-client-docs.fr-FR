---
title: Propriété canonique PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339941"
---
# <a name="pidlidtodotitle-canonical-property"></a><span data-ttu-id="86199-103">Propriété canonique PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="86199-103">PidLidToDoTitle Canonical Property</span></span>

  
  
<span data-ttu-id="86199-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86199-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86199-105">Contient le texte spécifié par l’utilisateur pour identifier cet objet de message dans une liste de choses à faire consolidée.</span><span class="sxs-lookup"><span data-stu-id="86199-105">Contains user-specifiable text to identify this message object in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86199-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="86199-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86199-107">dispidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="86199-107">dispidToDoTitle</span></span>  <br/> |
|<span data-ttu-id="86199-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="86199-108">Property set:</span></span>  <br/> |<span data-ttu-id="86199-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="86199-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="86199-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="86199-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="86199-111">0x000085A4</span><span class="sxs-lookup"><span data-stu-id="86199-111">0x000085A4</span></span>  <br/> |
|<span data-ttu-id="86199-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="86199-112">Data type:</span></span>  <br/> |<span data-ttu-id="86199-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="86199-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="86199-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="86199-114">Area:</span></span>  <br/> |<span data-ttu-id="86199-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="86199-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86199-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="86199-116">Remarks</span></span>

<span data-ttu-id="86199-117">Cette propriété ne doit pas être définie sur une tâche.</span><span class="sxs-lookup"><span data-stu-id="86199-117">This property must not be set on a task.</span></span> <span data-ttu-id="86199-118">Pour indiquer une propriété vide, ne définissez pas cette propriété sur la chaîne de longueur nulle, mais supprimez-la.</span><span class="sxs-lookup"><span data-stu-id="86199-118">To indicate an empty property, do not set this property to the zero-length string, but instead delete it.</span></span> 
  
<span data-ttu-id="86199-119">Lorsque vous signalez un objet de message et que la propriété n’existe pas, un client doit écrire la valeur de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="86199-119">When flagging a message object, and the property does not exist, a client should write the value of **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) to this property.</span></span>
  
<span data-ttu-id="86199-120">Dans une liste de choses à faire consolidée, si cette propriété n’existe pas, un client doit remplacer la valeur de la propriété **PR_NORMALIZED_SUBJECT** lors de l’affichage de cette propriété dans la liste des choses à faire.</span><span class="sxs-lookup"><span data-stu-id="86199-120">In a consolidated to-do list, if this property does not exist, a client should substitute the value of the **PR_NORMALIZED_SUBJECT** property when displaying this property in the to-do list.</span></span> 
  
<span data-ttu-id="86199-121">Sur un objet de brouillon de message, si le client implémente des indicateurs d’expéditeur, cette propriété doit être définie sur la même valeur que **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="86199-121">On a draft message object, if the client implements sender flags, this property should be set to the same value as **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="86199-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="86199-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86199-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="86199-123">Protocol specifications</span></span>

<span data-ttu-id="86199-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86199-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86199-125">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole</span><span class="sxs-lookup"><span data-stu-id="86199-125">Provides property set definitions and references to related Exchange Server protocol specifications</span></span>
    
<span data-ttu-id="86199-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86199-126">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86199-127">Spécifie les propriétés et les opérations liées au marquage.</span><span class="sxs-lookup"><span data-stu-id="86199-127">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86199-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="86199-128">Header files</span></span>

<span data-ttu-id="86199-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86199-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="86199-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="86199-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86199-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86199-131">See also</span></span>



[<span data-ttu-id="86199-132">Propriété canonique PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="86199-132">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
  
[<span data-ttu-id="86199-133">Propri�t� canonique PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="86199-133">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)


[<span data-ttu-id="86199-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="86199-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86199-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="86199-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86199-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="86199-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86199-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="86199-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

