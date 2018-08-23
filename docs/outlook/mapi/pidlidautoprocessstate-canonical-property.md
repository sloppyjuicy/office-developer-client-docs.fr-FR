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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b7e2db23b43383ca405ac58216b94a23d3257fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578338"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="88b72-103">Propriété canonique PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="88b72-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="88b72-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88b72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88b72-105">Définit les options qui sont utilisées dans le traitement automatique des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="88b72-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88b72-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="88b72-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88b72-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="88b72-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="88b72-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="88b72-108">Property set:</span></span>  <br/> |<span data-ttu-id="88b72-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="88b72-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="88b72-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="88b72-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="88b72-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="88b72-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="88b72-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="88b72-112">Data type:</span></span>  <br/> |<span data-ttu-id="88b72-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="88b72-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="88b72-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="88b72-114">Area:</span></span>  <br/> |<span data-ttu-id="88b72-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="88b72-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88b72-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="88b72-116">Remarks</span></span>

<span data-ttu-id="88b72-117">La propriété peut être absente, auquel cas la valeur par défaut « 0 x 00000000 » est utilisée.</span><span class="sxs-lookup"><span data-stu-id="88b72-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="88b72-118">Si la valeur, cette propriété doit avoir une des valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="88b72-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="88b72-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="88b72-119">**Value**</span></span>|<span data-ttu-id="88b72-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="88b72-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88b72-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88b72-121">0x00000000</span></span>  <br/> |<span data-ttu-id="88b72-122">Ne pas traiter automatiquement le message.</span><span class="sxs-lookup"><span data-stu-id="88b72-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="88b72-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="88b72-123">0x00000001</span></span>  <br/> |<span data-ttu-id="88b72-124">Traite le message automatiquement ou lorsque le message est ouvert.</span><span class="sxs-lookup"><span data-stu-id="88b72-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="88b72-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="88b72-125">0x00000002</span></span>  <br/> |<span data-ttu-id="88b72-126">Traite le message uniquement lorsque le message est ouvert.</span><span class="sxs-lookup"><span data-stu-id="88b72-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="88b72-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="88b72-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88b72-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="88b72-128">Protocol specifications</span></span>

<span data-ttu-id="88b72-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88b72-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88b72-130">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="88b72-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88b72-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88b72-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88b72-132">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="88b72-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88b72-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="88b72-133">Header files</span></span>

<span data-ttu-id="88b72-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88b72-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="88b72-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="88b72-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88b72-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88b72-136">See also</span></span>



[<span data-ttu-id="88b72-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="88b72-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88b72-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="88b72-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88b72-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="88b72-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88b72-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="88b72-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

