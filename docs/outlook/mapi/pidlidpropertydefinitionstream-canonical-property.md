---
title: Propriété canonique PidLidPropertyDefinitionStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f7f764d95c2fc36ba6af617333cb47d266cd2aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785338"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="a7eb6-103">Propriété canonique PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="a7eb6-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="a7eb6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7eb6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7eb6-105">Représente les définitions des champs définis par l’utilisateur et les paramètres de liaison de données de champs intégrés d’un message.</span><span class="sxs-lookup"><span data-stu-id="a7eb6-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7eb6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a7eb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7eb6-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="a7eb6-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="a7eb6-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="a7eb6-108">Property set:</span></span>  <br/> |<span data-ttu-id="a7eb6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a7eb6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a7eb6-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="a7eb6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a7eb6-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="a7eb6-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="a7eb6-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a7eb6-112">Data type:</span></span>  <br/> |<span data-ttu-id="a7eb6-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a7eb6-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a7eb6-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="a7eb6-114">Area:</span></span>  <br/> |<span data-ttu-id="a7eb6-115">Configuration d’exécution</span><span class="sxs-lookup"><span data-stu-id="a7eb6-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7eb6-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7eb6-116">Remarks</span></span>

<span data-ttu-id="a7eb6-117">La valeur de la propriété **PidLidPropertyDefinitionStream** est enregistrée dans le cadre de la définition de formulaire personnalisé pour le message.</span><span class="sxs-lookup"><span data-stu-id="a7eb6-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="a7eb6-118">La valeur de cette propriété est un objet stream binaire.</span><span class="sxs-lookup"><span data-stu-id="a7eb6-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="a7eb6-119">Pour plus d’informations sur la structure de ce flux de données, voir [La définition PropertyDefinition flux Structure](propertydefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="a7eb6-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a7eb6-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a7eb6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7eb6-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a7eb6-121">Protocol specifications</span></span>

<span data-ttu-id="a7eb6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7eb6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7eb6-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a7eb6-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7eb6-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a7eb6-124">Header files</span></span>

<span data-ttu-id="a7eb6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7eb6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7eb6-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a7eb6-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7eb6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7eb6-127">See also</span></span>



[<span data-ttu-id="a7eb6-128">Les champs et les éléments outlook</span><span class="sxs-lookup"><span data-stu-id="a7eb6-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="a7eb6-129">Ajoutez une définition pour un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a7eb6-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="a7eb6-130">Exemple de flux de la définition PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7eb6-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="a7eb6-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a7eb6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7eb6-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a7eb6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7eb6-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a7eb6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7eb6-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="a7eb6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

