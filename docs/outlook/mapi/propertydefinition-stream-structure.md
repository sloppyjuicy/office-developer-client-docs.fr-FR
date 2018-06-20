---
title: Structure de flux de la définition PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 289227ee171c2325cad0ed321dab4f635a0ca724
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786959"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="f1c6a-103">Structure de flux de la définition PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1c6a-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="f1c6a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1c6a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1c6a-105">Une structure de flux de la définition PropertyDefinition est un tableau de structures de flux [FieldDefinition](fielddefinition-stream-structure.md) qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un élément Microsoft Outlook et les paramètres de liaison de données pour certains champs prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="f1c6a-106">Vous pouvez manipuler par programme la structure de flux de la définition PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="f1c6a-107">Toutefois, vous pouvez obtenir des résultats similaires à l’aide du Concepteur de formulaires Outlook et, en particulier, la boîte de dialogue **Propriétés de** zone pour un contrôle lié aux données.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="f1c6a-108">Définitions de champ dans une structure de flux de la définition PropertyDefinition peuvent être une des deux formats : PropDefV1 et PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="f1c6a-109">Outlook prend en charge à la fois PropDefV1 et PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="f1c6a-110">Toutes les définitions de champ dans une structure de flux de la définition PropertyDefinition unique doivent être du même format.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="f1c6a-111">Pour plus d’informations sur la différence entre PropDefV1 et PropDefV2, voir [FieldDefinition flux Structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="f1c6a-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="f1c6a-112">Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="f1c6a-113">Version : Mot (2 octets), le format des définitions de champ dans la définition PropertyDefinition du flux de structure.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="f1c6a-114">Le tableau suivant présente les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="f1c6a-115">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f1c6a-115">**Value**</span></span>|<span data-ttu-id="f1c6a-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1c6a-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="f1c6a-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="f1c6a-117">0x0102</span></span>  <br/> |<span data-ttu-id="f1c6a-118">Format est PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="f1c6a-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="f1c6a-119">0x0103</span></span>  <br/> |<span data-ttu-id="f1c6a-120">Format est PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="f1c6a-121">FieldDefinitionCount : DWORD (4 octets), le nombre de définitions de champ dans ce flux.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="f1c6a-122">Il s’agit du nombre d’éléments de tableau dans l’élément de données FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="f1c6a-123">FieldDefinitions : Un tableau de structures de flux FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="f1c6a-124">Le nombre de ce tableau est égal à l’élément de données FieldDefinitionCount.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1c6a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1c6a-125">See also</span></span>

- [<span data-ttu-id="f1c6a-126">Les champs et les éléments outlook</span><span class="sxs-lookup"><span data-stu-id="f1c6a-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="f1c6a-127">Ajoutez une définition pour un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f1c6a-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="f1c6a-128">Exemple de flux de la définition PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1c6a-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="f1c6a-129">Structures de flux de données</span><span class="sxs-lookup"><span data-stu-id="f1c6a-129">Stream Structures</span></span>](stream-structures.md)

