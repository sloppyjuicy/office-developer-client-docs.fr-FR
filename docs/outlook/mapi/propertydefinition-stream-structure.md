---
title: Structure de flux PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438588"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="9bbda-103">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="9bbda-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="9bbda-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bbda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bbda-105">Une structure de flux PropertyDefinition est un tableau de structures de flux [FieldDefinition](fielddefinition-stream-structure.md) qui contiennent des définitions pour tous les champs définis par l’utilisateur dans un élément Microsoft Outlook et des paramètres de liaison de données pour certains champs intégrés.</span><span class="sxs-lookup"><span data-stu-id="9bbda-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="9bbda-106">Vous pouvez manipuler par programme la structure de flux PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9bbda-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="9bbda-107">Toutefois, vous pouvez obtenir des résultats similaires à  l’aide du Concepteur de formulaires Outlook et, en particulier, de la boîte de dialogue Propriétés d’un contrôle lié aux données.</span><span class="sxs-lookup"><span data-stu-id="9bbda-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="9bbda-108">Les définitions de champ dans une structure de flux PropertyDefinition peuvent être l’un des deux formats : PropDefV1 et PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="9bbda-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="9bbda-109">Outlook prend en charge PropDefV1 et PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="9bbda-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="9bbda-110">Toutes les définitions de champ dans une structure de flux PropertyDefinition unique doivent être au même format.</span><span class="sxs-lookup"><span data-stu-id="9bbda-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="9bbda-111">Pour plus d’informations sur la différence entre PropDefV1 et PropDefV2, voir Structure de flux [FieldDefinition.](fielddefinition-stream-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bbda-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="9bbda-112">Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9bbda-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="9bbda-113">Version : WORD (2 octets), format des définitions de champ dans la structure de flux PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9bbda-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="9bbda-114">Le tableau suivant montre les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="9bbda-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="9bbda-115">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9bbda-115">**Value**</span></span>|<span data-ttu-id="9bbda-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="9bbda-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="9bbda-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="9bbda-117">0x0102</span></span>  <br/> |<span data-ttu-id="9bbda-118">Le format est PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="9bbda-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="9bbda-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="9bbda-119">0x0103</span></span>  <br/> |<span data-ttu-id="9bbda-120">Le format est PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="9bbda-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="9bbda-121">FieldDefinitionCount : DWORD (4 octets), nombre de définitions de champ dans ce flux.</span><span class="sxs-lookup"><span data-stu-id="9bbda-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="9bbda-122">Il s’agit du nombre d’éléments de tableau dans l’élément de données FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="9bbda-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="9bbda-123">FieldDefinitions : tableau de structures de flux FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="9bbda-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="9bbda-124">Le nombre de ce tableau est égal à l’élément de données FieldDefinitionCount.</span><span class="sxs-lookup"><span data-stu-id="9bbda-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bbda-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bbda-125">See also</span></span>

- [<span data-ttu-id="9bbda-126">Éléments et champs Outlook</span><span class="sxs-lookup"><span data-stu-id="9bbda-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="9bbda-127">Ajouter une définition pour un nouveau champ User-Defined de recherche</span><span class="sxs-lookup"><span data-stu-id="9bbda-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="9bbda-128">Exemple de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="9bbda-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="9bbda-129">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="9bbda-129">Stream Structures</span></span>](stream-structures.md)

