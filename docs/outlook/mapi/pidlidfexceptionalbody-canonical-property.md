---
title: Propriété canonique PidLidFExceptionalBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalBody
api_type:
- COM
ms.assetid: 327516e8-ed3f-40fc-9604-03a70aecef5a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327460"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="a76b3-103">Propriété canonique PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="a76b3-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="a76b3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a76b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a76b3-105">Indique que l’objet message incorporé d’exception possède un corps qui diffère de l’objet calendrier périodique.</span><span class="sxs-lookup"><span data-stu-id="a76b3-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a76b3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a76b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a76b3-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="a76b3-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="a76b3-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="a76b3-108">Property set:</span></span>  <br/> |<span data-ttu-id="a76b3-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a76b3-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a76b3-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="a76b3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a76b3-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="a76b3-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="a76b3-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a76b3-112">Data type:</span></span>  <br/> |<span data-ttu-id="a76b3-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a76b3-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a76b3-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a76b3-114">Area:</span></span>  <br/> |<span data-ttu-id="a76b3-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="a76b3-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a76b3-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a76b3-116">Remarks</span></span>

<span data-ttu-id="a76b3-117">Si la valeur de cette propriété est TRUE, l’objet message incorporé d’exception doit avoir un corps.</span><span class="sxs-lookup"><span data-stu-id="a76b3-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="a76b3-118">Si la valeur de cette propriété est FALSE ou si la propriété n’existe pas, un client ou un serveur doit obtenir le corps à partir de l’objet calendrier périodique.</span><span class="sxs-lookup"><span data-stu-id="a76b3-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a76b3-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a76b3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a76b3-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a76b3-120">Protocol specifications</span></span>

<span data-ttu-id="a76b3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a76b3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a76b3-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="a76b3-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a76b3-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a76b3-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a76b3-124">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="a76b3-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a76b3-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a76b3-125">Header files</span></span>

<span data-ttu-id="a76b3-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a76b3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a76b3-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a76b3-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a76b3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a76b3-128">See also</span></span>



[<span data-ttu-id="a76b3-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a76b3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a76b3-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a76b3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a76b3-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a76b3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a76b3-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a76b3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

