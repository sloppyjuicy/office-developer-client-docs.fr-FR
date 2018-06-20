---
title: Propriété canonique PidLidAutoProcessState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 86ef98ac7b4084de3a96210298fe0d5509d12103
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785068"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="9bb68-103">Propriété canonique PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="9bb68-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="9bb68-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9bb68-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9bb68-105">Définit les options qui sont utilisées dans le traitement automatique des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="9bb68-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bb68-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9bb68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bb68-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="9bb68-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="9bb68-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="9bb68-108">Property set:</span></span>  <br/> |<span data-ttu-id="9bb68-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9bb68-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9bb68-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="9bb68-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9bb68-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="9bb68-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="9bb68-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9bb68-112">Data type:</span></span>  <br/> |<span data-ttu-id="9bb68-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9bb68-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9bb68-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="9bb68-114">Area:</span></span>  <br/> |<span data-ttu-id="9bb68-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="9bb68-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bb68-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="9bb68-116">Remarks</span></span>

<span data-ttu-id="9bb68-117">La propriété peut être absente, auquel cas la valeur par défaut « 0 x 00000000 » est utilisée.</span><span class="sxs-lookup"><span data-stu-id="9bb68-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="9bb68-118">Si la valeur, cette propriété doit avoir une des valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9bb68-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="9bb68-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9bb68-119">**Value**</span></span>|<span data-ttu-id="9bb68-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="9bb68-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9bb68-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9bb68-121">0x00000000</span></span>  <br/> |<span data-ttu-id="9bb68-122">Ne pas traiter automatiquement le message.</span><span class="sxs-lookup"><span data-stu-id="9bb68-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="9bb68-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bb68-123">0x00000001</span></span>  <br/> |<span data-ttu-id="9bb68-124">Traite le message automatiquement ou lorsque le message est ouvert.</span><span class="sxs-lookup"><span data-stu-id="9bb68-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="9bb68-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9bb68-125">0x00000002</span></span>  <br/> |<span data-ttu-id="9bb68-126">Traite le message uniquement lorsque le message est ouvert.</span><span class="sxs-lookup"><span data-stu-id="9bb68-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9bb68-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9bb68-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bb68-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9bb68-128">Protocol specifications</span></span>

<span data-ttu-id="9bb68-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bb68-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bb68-130">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="9bb68-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9bb68-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bb68-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bb68-132">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="9bb68-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9bb68-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9bb68-133">Header files</span></span>

<span data-ttu-id="9bb68-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bb68-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bb68-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9bb68-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bb68-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bb68-136">See also</span></span>



[<span data-ttu-id="9bb68-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9bb68-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bb68-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9bb68-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bb68-139">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9bb68-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bb68-140">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="9bb68-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

