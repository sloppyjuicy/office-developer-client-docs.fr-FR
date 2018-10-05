---
title: Propriété canonique PidTagDefaultPostMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0ab904625d3a23462a4fedf3b64f49c54b34ad28
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401726"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="904ff-103">Propriété canonique PidTagDefaultPostMessageClass</span><span class="sxs-lookup"><span data-stu-id="904ff-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="904ff-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="904ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="904ff-105">Contient le nom d’une classe de Message du formulaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="904ff-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="904ff-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="904ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="904ff-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="904ff-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="904ff-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="904ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="904ff-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="904ff-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="904ff-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="904ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="904ff-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="904ff-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="904ff-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="904ff-112">Area:</span></span>  <br/> |<span data-ttu-id="904ff-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="904ff-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="904ff-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="904ff-114">Remarks</span></span>

<span data-ttu-id="904ff-115">Si cette propriété est définie sur un dossier, soit de la valeur doit contenir exactement la classe de message de base (par exemple, « IPM. Contact » pour un dossier de contacts ou un « IPM. Rendez-vous » pour un dossier de calendrier), ou commencer par la classe de message de base (par exemple, « IPM. Contact.MyContact »).</span><span class="sxs-lookup"><span data-stu-id="904ff-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="904ff-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="904ff-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="904ff-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="904ff-117">Protocol specifications</span></span>

<span data-ttu-id="904ff-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="904ff-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="904ff-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="904ff-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="904ff-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="904ff-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="904ff-121">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="904ff-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="904ff-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="904ff-122">Header files</span></span>

<span data-ttu-id="904ff-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="904ff-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="904ff-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="904ff-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="904ff-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="904ff-125">Mapitags.h</span></span>
  
> <span data-ttu-id="904ff-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="904ff-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="904ff-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="904ff-127">See also</span></span>



[<span data-ttu-id="904ff-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="904ff-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="904ff-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="904ff-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="904ff-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="904ff-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="904ff-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="904ff-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

