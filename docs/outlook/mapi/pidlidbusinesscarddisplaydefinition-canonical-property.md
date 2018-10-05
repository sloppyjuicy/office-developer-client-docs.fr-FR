---
title: Propriété canonique PidLidBusinessCardDisplayDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399101"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="807da-103">Propriété canonique PidLidBusinessCardDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="807da-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="807da-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="807da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="807da-105">Contient des détails de personnalisation de l’utilisateur pour l’affichage d’un contact dans une carte de visite.</span><span class="sxs-lookup"><span data-stu-id="807da-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="807da-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="807da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="807da-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="807da-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="807da-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="807da-108">Property set:</span></span>  <br/> |<span data-ttu-id="807da-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="807da-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="807da-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="807da-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="807da-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="807da-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="807da-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="807da-112">Data type:</span></span>  <br/> |<span data-ttu-id="807da-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="807da-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="807da-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="807da-114">Area:</span></span>  <br/> |<span data-ttu-id="807da-115">Contact</span><span class="sxs-lookup"><span data-stu-id="807da-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="807da-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="807da-116">Remarks</span></span>

<span data-ttu-id="807da-117">La disposition d’une carte de visite peut être représentée comme une image et un nombre de champs de texte.</span><span class="sxs-lookup"><span data-stu-id="807da-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="807da-118">L’image peut être une photo du contact, ou une image de la carte.</span><span class="sxs-lookup"><span data-stu-id="807da-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="807da-119">Champs de texte se composent d’une valeur à partir d’un autre jeu de propriétés sur le contact et une chaîne d’étiquette personnalisée facultative fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="807da-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="807da-120">Notez que les valeurs multiples octets sont stockés dans le format little-endian dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="807da-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="807da-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="807da-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="807da-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="807da-122">Protocol specifications</span></span>

<span data-ttu-id="807da-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="807da-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="807da-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="807da-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="807da-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="807da-125">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="807da-126">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="807da-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="807da-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="807da-127">Header files</span></span>

<span data-ttu-id="807da-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="807da-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="807da-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="807da-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="807da-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="807da-130">See also</span></span>



[<span data-ttu-id="807da-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="807da-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="807da-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="807da-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="807da-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="807da-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="807da-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="807da-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

