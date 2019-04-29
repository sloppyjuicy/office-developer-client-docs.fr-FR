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
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="369d0-103">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="369d0-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="369d0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="369d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="369d0-105">Une structure de flux PropertyDefinition est un tableau de structures de flux [FieldDefinition](fielddefinition-stream-structure.md) contenant des définitions pour tous les champs définis par l'utilisateur dans un élément Microsoft Outlook et des paramètres de liaison de données pour certains champs intégrés.</span><span class="sxs-lookup"><span data-stu-id="369d0-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="369d0-106">Vous pouvez manipuler la structure de flux PropertyDefinition par programmation.</span><span class="sxs-lookup"><span data-stu-id="369d0-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="369d0-107">Toutefois, vous pouvez obtenir des résultats similaires à l'aide du concepteur de formulaires Outlook et, en particulier, de la boîte de dialogue **Propriétés** d'un contrôle lié aux données.</span><span class="sxs-lookup"><span data-stu-id="369d0-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="369d0-108">Les définitions de champ dans une structure de flux PropertyDefinition peuvent être l'un des deux formats suivants: PropDefV1 et PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="369d0-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="369d0-109">Outlook prend en charge à la fois PropDefV1 et PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="369d0-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="369d0-110">Toutes les définitions de champ d'une structure de flux PropertyDefinition unique doivent être du même format.</span><span class="sxs-lookup"><span data-stu-id="369d0-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="369d0-111">Pour plus d'informations sur la façon dont PropDefV1 et PropDefV2 diffèrent, voir [FieldDefinition Stream structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="369d0-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="369d0-112">Les éléments de données dans ce flux sont stockés dans l'ordre d'octet Little-endian, immédiatement suivant l'ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="369d0-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="369d0-113">Version: WORD (2 octets), le format des définitions de champ dans la structure de flux PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="369d0-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="369d0-114">Le tableau suivant montre les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="369d0-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="369d0-115">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="369d0-115">**Value**</span></span>|<span data-ttu-id="369d0-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="369d0-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="369d0-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="369d0-117">0x0102</span></span>  <br/> |<span data-ttu-id="369d0-118">Le format est PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="369d0-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="369d0-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="369d0-119">0x0103</span></span>  <br/> |<span data-ttu-id="369d0-120">Le format est PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="369d0-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="369d0-121">FieldDefinitionCount: DWORD (4 octets), le nombre de définitions de champ dans ce flux.</span><span class="sxs-lookup"><span data-stu-id="369d0-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="369d0-122">Il s'agit du nombre d'éléments de tableau dans l'élément de données FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="369d0-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="369d0-123">FieldDefinitions: tableau de structures de flux FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="369d0-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="369d0-124">Le nombre de ce tableau est égal à l'élément de données FieldDefinitionCount.</span><span class="sxs-lookup"><span data-stu-id="369d0-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="369d0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="369d0-125">See also</span></span>

- [<span data-ttu-id="369d0-126">Éléments et champs Outlook</span><span class="sxs-lookup"><span data-stu-id="369d0-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="369d0-127">Ajouter une définition pour un nouveau champ défini par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="369d0-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="369d0-128">Exemple de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="369d0-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="369d0-129">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="369d0-129">Stream Structures</span></span>](stream-structures.md)

