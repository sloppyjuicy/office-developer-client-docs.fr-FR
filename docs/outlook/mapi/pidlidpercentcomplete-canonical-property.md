---
title: Propri t canonique PidLidPercentComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidPercentComplete
api_type:
- COM
ms.assetid: e63792b1-9580-4702-a6d7-dd3ae5007a4a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 870b4e0edb360ac36525f94b0605af930eee8fa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357973"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="56e0c-103">Propri t canonique PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="56e0c-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="56e0c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56e0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56e0c-105">Indique la progression de l’utilisateur sur une tâche.</span><span class="sxs-lookup"><span data-stu-id="56e0c-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56e0c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="56e0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56e0c-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="56e0c-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="56e0c-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="56e0c-108">Property set:</span></span>  <br/> |<span data-ttu-id="56e0c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="56e0c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="56e0c-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="56e0c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="56e0c-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="56e0c-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="56e0c-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="56e0c-112">Data type:</span></span>  <br/> |<span data-ttu-id="56e0c-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="56e0c-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="56e0c-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="56e0c-114">Area:</span></span>  <br/> |<span data-ttu-id="56e0c-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="56e0c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56e0c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="56e0c-116">Remarks</span></span>

<span data-ttu-id="56e0c-117">La valeur de cette propriété doit être un nombre supérieur ou égal à 0.0 et inférieur ou égal à 1.0, où 1.0 indique que le travail est terminé et 0.0 indique que le travail n’a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="56e0c-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="56e0c-118">Pour un objet de message avec marquage dans le temps, la valeur de cette propriété doit être définie sur 1.0 si l’objet est marqué comme terminé et doit être définie sur 0.0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="56e0c-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="56e0c-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="56e0c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56e0c-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="56e0c-120">Protocol specifications</span></span>

<span data-ttu-id="56e0c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56e0c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56e0c-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="56e0c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56e0c-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56e0c-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56e0c-124">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="56e0c-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="56e0c-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56e0c-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56e0c-126">Spécifie les propriétés et les opérations liées au marquage.</span><span class="sxs-lookup"><span data-stu-id="56e0c-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="56e0c-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56e0c-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56e0c-128">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="56e0c-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="56e0c-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56e0c-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56e0c-130">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="56e0c-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="56e0c-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56e0c-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56e0c-132">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="56e0c-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56e0c-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="56e0c-133">Header files</span></span>

<span data-ttu-id="56e0c-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56e0c-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="56e0c-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="56e0c-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56e0c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56e0c-136">See also</span></span>



[<span data-ttu-id="56e0c-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="56e0c-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56e0c-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="56e0c-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56e0c-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="56e0c-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56e0c-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="56e0c-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

