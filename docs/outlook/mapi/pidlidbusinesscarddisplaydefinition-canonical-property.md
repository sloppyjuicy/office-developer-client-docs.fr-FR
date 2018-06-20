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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 34d29b9a15cc6f5a3f88a6477738eb63904e1fdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785085"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a><span data-ttu-id="cfb0a-103">Propriété canonique PidLidBusinessCardDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="cfb0a-103">PidLidBusinessCardDisplayDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="cfb0a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cfb0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cfb0a-105">Contient des détails de personnalisation de l’utilisateur pour l’affichage d’un contact dans une carte de visite.</span><span class="sxs-lookup"><span data-stu-id="cfb0a-105">Contains user-customization details for displaying a contact as a business card.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cfb0a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cfb0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cfb0a-107">dispidBCDisplayDefinition</span><span class="sxs-lookup"><span data-stu-id="cfb0a-107">dispidBCDisplayDefinition</span></span>  <br/> |
|<span data-ttu-id="cfb0a-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="cfb0a-108">Property set:</span></span>  <br/> |<span data-ttu-id="cfb0a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="cfb0a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="cfb0a-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="cfb0a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cfb0a-111">0x00008040</span><span class="sxs-lookup"><span data-stu-id="cfb0a-111">0x00008040</span></span>  <br/> |
|<span data-ttu-id="cfb0a-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cfb0a-112">Data type:</span></span>  <br/> |<span data-ttu-id="cfb0a-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cfb0a-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cfb0a-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="cfb0a-114">Area:</span></span>  <br/> |<span data-ttu-id="cfb0a-115">Contact</span><span class="sxs-lookup"><span data-stu-id="cfb0a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfb0a-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="cfb0a-116">Remarks</span></span>

<span data-ttu-id="cfb0a-117">La disposition d’une carte de visite peut être représentée comme une image et un nombre de champs de texte.</span><span class="sxs-lookup"><span data-stu-id="cfb0a-117">The layout of a business card can be represented as an image and a number of text fields.</span></span> <span data-ttu-id="cfb0a-118">L’image peut être une photo du contact, ou une image de la carte.</span><span class="sxs-lookup"><span data-stu-id="cfb0a-118">The image can be either a contact photo, or a card picture.</span></span> <span data-ttu-id="cfb0a-119">Champs de texte se composent d’une valeur à partir d’un autre jeu de propriétés sur le contact et une chaîne d’étiquette personnalisée facultative fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cfb0a-119">Text fields consist of a value from another property set on the contact and an optional customized label string provided by the user.</span></span> <span data-ttu-id="cfb0a-120">Notez que les valeurs multiples octets sont stockés dans le format little-endian dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cfb0a-120">Note that multi-byte values are stored in little-endian format in the buffer.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cfb0a-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cfb0a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cfb0a-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="cfb0a-122">Protocol specifications</span></span>

<span data-ttu-id="cfb0a-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfb0a-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfb0a-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="cfb0a-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cfb0a-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfb0a-125">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfb0a-126">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="cfb0a-126">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cfb0a-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cfb0a-127">Header files</span></span>

<span data-ttu-id="cfb0a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cfb0a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="cfb0a-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cfb0a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cfb0a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfb0a-130">See also</span></span>



[<span data-ttu-id="cfb0a-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cfb0a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cfb0a-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cfb0a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cfb0a-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cfb0a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cfb0a-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="cfb0a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

