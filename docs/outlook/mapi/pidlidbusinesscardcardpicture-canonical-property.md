---
title: Propriété canonique PidLidBusinessCardCardPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b83316b599ea9ee62bde78cbd734dfb6b2d8b80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588495"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a><span data-ttu-id="3b8d2-103">Propriété canonique PidLidBusinessCardCardPicture</span><span class="sxs-lookup"><span data-stu-id="3b8d2-103">PidLidBusinessCardCardPicture Canonical Property</span></span>

  
  
<span data-ttu-id="3b8d2-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b8d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b8d2-105">Contient l’image à utiliser dans une carte de visite.</span><span class="sxs-lookup"><span data-stu-id="3b8d2-105">Contains the image to use on a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b8d2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3b8d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b8d2-107">dispidBCCardPicture</span><span class="sxs-lookup"><span data-stu-id="3b8d2-107">dispidBCCardPicture</span></span>  <br/> |
|<span data-ttu-id="3b8d2-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="3b8d2-108">Property set:</span></span>  <br/> |<span data-ttu-id="3b8d2-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3b8d2-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3b8d2-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="3b8d2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3b8d2-111">0x00008041</span><span class="sxs-lookup"><span data-stu-id="3b8d2-111">0x00008041</span></span>  <br/> |
|<span data-ttu-id="3b8d2-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3b8d2-112">Data type:</span></span>  <br/> |<span data-ttu-id="3b8d2-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3b8d2-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3b8d2-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3b8d2-114">Area:</span></span>  <br/> |<span data-ttu-id="3b8d2-115">Contact</span><span class="sxs-lookup"><span data-stu-id="3b8d2-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b8d2-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b8d2-116">Remarks</span></span>

<span data-ttu-id="3b8d2-117">La valeur de cette propriété doit être un graphique réseau portable (PNG) ou un flux au format JPEG.</span><span class="sxs-lookup"><span data-stu-id="3b8d2-117">The value of this property must be either a portable network graphics (PNG) or JPEG stream.</span></span> <span data-ttu-id="3b8d2-118">Cette propriété doit être utilisée conjointement avec la propriété **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) comme suit : **dispidBCCardPicture** ne doit pas être présent sur un contact se ** dispidBCDisplayDefinition** n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="3b8d2-118">This property should be used in conjunction with the **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) property as follows: **dispidBCCardPicture** should not be present on a contact if **dispidBCDisplayDefinition** is not present.</span></span> <span data-ttu-id="3b8d2-119">Cette propriété également ne doit pas être présente si les données **dispidBCCardPicture** ne requièrent pas une image de la carte.</span><span class="sxs-lookup"><span data-stu-id="3b8d2-119">This property also should not be present if the data in **dispidBCCardPicture** does not require a card image.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3b8d2-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3b8d2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b8d2-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3b8d2-121">Protocol specifications</span></span>

<span data-ttu-id="3b8d2-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b8d2-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b8d2-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="3b8d2-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b8d2-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b8d2-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b8d2-125">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="3b8d2-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b8d2-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3b8d2-126">Header files</span></span>

<span data-ttu-id="3b8d2-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b8d2-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b8d2-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3b8d2-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b8d2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b8d2-129">See also</span></span>



[<span data-ttu-id="3b8d2-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3b8d2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b8d2-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3b8d2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b8d2-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3b8d2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b8d2-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3b8d2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

