---
title: Propriété canonique PidLidTaskFCreator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dfb49fafcc2dc368e84786b526869e0447ccaf8c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387180"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="265c0-103">Propriété canonique PidLidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="265c0-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="265c0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="265c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="265c0-105">Indique que la tâche a été initialement créée par l’utilisateur actuel ou de l’agent utilisateur au lieu de transformation d’une demande de tâche.</span><span class="sxs-lookup"><span data-stu-id="265c0-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="265c0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="265c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="265c0-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="265c0-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="265c0-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="265c0-108">Property set:</span></span>  <br/> |<span data-ttu-id="265c0-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="265c0-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="265c0-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="265c0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="265c0-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="265c0-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="265c0-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="265c0-112">Data type:</span></span>  <br/> |<span data-ttu-id="265c0-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="265c0-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="265c0-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="265c0-114">Area:</span></span>  <br/> |<span data-ttu-id="265c0-115">Task</span><span class="sxs-lookup"><span data-stu-id="265c0-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="265c0-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="265c0-116">Remarks</span></span>

<span data-ttu-id="265c0-117">Le client définit cette propriété sur TRUE lorsque l’utilisateur crée la tâche et la valeur FALSE lorsque la tâche est affectée par un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="265c0-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="265c0-118">Si cette propriété n’est pas définie, la valeur TRUE est supposée.</span><span class="sxs-lookup"><span data-stu-id="265c0-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="265c0-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="265c0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="265c0-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="265c0-120">Protocol specifications</span></span>

<span data-ttu-id="265c0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="265c0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="265c0-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="265c0-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="265c0-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="265c0-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="265c0-124">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="265c0-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="265c0-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="265c0-125">Header files</span></span>

<span data-ttu-id="265c0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="265c0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="265c0-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="265c0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="265c0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="265c0-128">See also</span></span>



[<span data-ttu-id="265c0-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="265c0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="265c0-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="265c0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="265c0-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="265c0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="265c0-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="265c0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

