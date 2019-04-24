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
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320425"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="0d12d-103">Propriété canonique PidTagUrlComponentName</span><span class="sxs-lookup"><span data-stu-id="0d12d-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="0d12d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d12d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d12d-105">Nom du composant d'URL d'un message.</span><span class="sxs-lookup"><span data-stu-id="0d12d-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d12d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0d12d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d12d-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="0d12d-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="0d12d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0d12d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0d12d-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="0d12d-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="0d12d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0d12d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0d12d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d12d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0d12d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0d12d-112">Area:</span></span>  <br/> |<span data-ttu-id="0d12d-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="0d12d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d12d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d12d-114">Remarks</span></span>

<span data-ttu-id="0d12d-115">Ces propriétés doivent être uniques dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="0d12d-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="0d12d-116">Si elle n'est pas définie lors de la création du message, la Banque de messages doit définir ces propriétés en fonction de différentes propriétés de message, en fonction de la classe de message.</span><span class="sxs-lookup"><span data-stu-id="0d12d-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="0d12d-117">Par exemple, le **IPM. Remarque** et \*\*IPM. \*\*Cette propriété doit être définie pour les messages de rendEz-vous en fonction de la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et de la propriété \*\*IPM. \*\*Cette propriété doit être définie pour les messages de contact en fonction de la propriété **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0d12d-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="0d12d-118">Pour la plupart des autres classes de message, cette propriété doit être basée sur la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0d12d-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d12d-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="0d12d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d12d-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="0d12d-120">Protocol specifications</span></span>

<span data-ttu-id="0d12d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d12d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d12d-122">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="0d12d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d12d-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d12d-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d12d-124">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="0d12d-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0d12d-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d12d-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d12d-126">Encode et décode les objets message et Attachment en une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="0d12d-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d12d-127">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="0d12d-127">Header files</span></span>

<span data-ttu-id="0d12d-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0d12d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d12d-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0d12d-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="0d12d-130">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0d12d-130">Mapitags.h</span></span>
  
> <span data-ttu-id="0d12d-131">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="0d12d-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d12d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d12d-132">See also</span></span>



[<span data-ttu-id="0d12d-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0d12d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d12d-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0d12d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d12d-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0d12d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d12d-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0d12d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

