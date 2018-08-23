---
title: Propriété canonique PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2868533e0383309e013bb82aaa4300a0a40e335a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577512"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="b82d0-103">Propriété canonique PidTagControlId</span><span class="sxs-lookup"><span data-stu-id="b82d0-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="b82d0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b82d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b82d0-105">Contient un identificateur unique pour un contrôle utilisé dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b82d0-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b82d0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b82d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b82d0-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="b82d0-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="b82d0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b82d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b82d0-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="b82d0-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="b82d0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b82d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="b82d0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b82d0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b82d0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b82d0-112">Area:</span></span>  <br/> |<span data-ttu-id="b82d0-113">Afficher une table MAPI</span><span class="sxs-lookup"><span data-stu-id="b82d0-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b82d0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b82d0-114">Remarks</span></span>

<span data-ttu-id="b82d0-115">Cette propriété contient un identificateur unique pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b82d0-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="b82d0-116">Cet identificateur doit contenir une structure [GUID](guid.md) et une valeur de type **LONG**binary.</span><span class="sxs-lookup"><span data-stu-id="b82d0-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="b82d0-117">Tous les contrôles dans la boîte de dialogue doivent utiliser le même **GUID** pour identifier le fournisseur de services, et chaque contrôle doit utiliser un unique valeur de **type LONG** pour s’assurer que les contrôles n’entrent pas en conflit.</span><span class="sxs-lookup"><span data-stu-id="b82d0-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="b82d0-118">Cette propriété est utilisée dans les notifications.</span><span class="sxs-lookup"><span data-stu-id="b82d0-118">This property is used in notifications.</span></span> <span data-ttu-id="b82d0-119">Par exemple, notifications envoyées sur le tableau de l’affichage doivent définir cette propriété pour identifier le contrôle à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="b82d0-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b82d0-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b82d0-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b82d0-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b82d0-121">Header files</span></span>

<span data-ttu-id="b82d0-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b82d0-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="b82d0-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b82d0-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="b82d0-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b82d0-124">Mapitags.h</span></span>
  
> <span data-ttu-id="b82d0-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="b82d0-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b82d0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b82d0-126">See also</span></span>



[<span data-ttu-id="b82d0-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b82d0-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b82d0-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b82d0-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b82d0-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b82d0-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b82d0-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b82d0-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

