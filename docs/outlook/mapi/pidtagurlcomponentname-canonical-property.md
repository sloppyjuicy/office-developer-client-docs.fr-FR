---
title: Propriété canonique PidTagUrlComponentName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3a2b0939bbfa5143e4bd99e74b0f84e3ca7efb12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786905"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="3b45c-103">Propriété canonique PidTagUrlComponentName</span><span class="sxs-lookup"><span data-stu-id="3b45c-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="3b45c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b45c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b45c-105">Le nom du composant URL pour un message.</span><span class="sxs-lookup"><span data-stu-id="3b45c-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b45c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3b45c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b45c-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3b45c-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3b45c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3b45c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3b45c-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="3b45c-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="3b45c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3b45c-110">Data type:</span></span>  <br/> |<span data-ttu-id="3b45c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3b45c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3b45c-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="3b45c-112">Area:</span></span>  <br/> |<span data-ttu-id="3b45c-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="3b45c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b45c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b45c-114">Remarks</span></span>

<span data-ttu-id="3b45c-115">Ces propriétés doivent être uniques au sein d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="3b45c-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="3b45c-116">Si ce n’est pas ensemble lorsque le message est créé, la banque de messages doit définir ces propriétés en fonction de diverses propriétés de message, en fonction de la classe de message.</span><span class="sxs-lookup"><span data-stu-id="3b45c-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="3b45c-117">Par exemple, le **IPM. Note** et **IPM. Rendez-vous** messages doivent utilisent cette propriété en fonction de la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et le **IPM. Contact** cette propriété doivent être définie en fonction de la propriété **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) pour messages.</span><span class="sxs-lookup"><span data-stu-id="3b45c-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="3b45c-118">Pour la plupart des autres classes de messages, cette propriété doit être basée sur la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3b45c-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3b45c-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3b45c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b45c-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3b45c-120">Protocol specifications</span></span>

<span data-ttu-id="3b45c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b45c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b45c-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="3b45c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b45c-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b45c-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b45c-124">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3b45c-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="3b45c-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b45c-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b45c-126">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="3b45c-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b45c-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3b45c-127">Header files</span></span>

<span data-ttu-id="3b45c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b45c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b45c-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3b45c-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="3b45c-130">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3b45c-130">Mapitags.h</span></span>
  
> <span data-ttu-id="3b45c-131">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3b45c-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b45c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b45c-132">See also</span></span>



[<span data-ttu-id="3b45c-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3b45c-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b45c-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3b45c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b45c-135">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3b45c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b45c-136">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3b45c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

