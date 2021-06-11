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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0918c15d87219c1ee20b177ae21e718e0289cf04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342062"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="43821-103">Propriété canonique PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="43821-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="43821-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43821-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43821-105">Spécifie les options utilisées dans le traitement automatique des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="43821-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43821-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="43821-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43821-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="43821-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="43821-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="43821-108">Property set:</span></span>  <br/> |<span data-ttu-id="43821-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="43821-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="43821-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="43821-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="43821-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="43821-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="43821-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="43821-112">Data type:</span></span>  <br/> |<span data-ttu-id="43821-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="43821-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="43821-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="43821-114">Area:</span></span>  <br/> |<span data-ttu-id="43821-115">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="43821-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43821-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="43821-116">Remarks</span></span>

<span data-ttu-id="43821-117">La propriété peut être absente, auquel cas la valeur par défaut de « 0x00000000 » est utilisée.</span><span class="sxs-lookup"><span data-stu-id="43821-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="43821-118">Si elle est définie, cette propriété doit être définie sur l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="43821-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="43821-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="43821-119">**Value**</span></span>|<span data-ttu-id="43821-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="43821-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="43821-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43821-121">0x00000000</span></span>  <br/> |<span data-ttu-id="43821-122">Ne pas traiter automatiquement le message.</span><span class="sxs-lookup"><span data-stu-id="43821-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="43821-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="43821-123">0x00000001</span></span>  <br/> |<span data-ttu-id="43821-124">Traiter le message automatiquement ou lorsque le message est ouvert.</span><span class="sxs-lookup"><span data-stu-id="43821-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="43821-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="43821-125">0x00000002</span></span>  <br/> |<span data-ttu-id="43821-126">Traiter le message uniquement lorsque le message est ouvert.</span><span class="sxs-lookup"><span data-stu-id="43821-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="43821-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="43821-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43821-128">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="43821-128">Protocol specifications</span></span>

<span data-ttu-id="43821-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43821-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43821-130">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="43821-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43821-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43821-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43821-132">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="43821-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43821-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="43821-133">Header files</span></span>

<span data-ttu-id="43821-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43821-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="43821-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="43821-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43821-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43821-136">See also</span></span>



[<span data-ttu-id="43821-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="43821-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43821-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="43821-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43821-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="43821-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43821-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="43821-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

