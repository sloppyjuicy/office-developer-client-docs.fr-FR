---
title: Structure de flux PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328482"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="ca97a-103">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="ca97a-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="ca97a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca97a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca97a-105">Une structure de flux PropertyDefinition est un tableau de structures de flux [FieldDefinition](fielddefinition-stream-structure.md) contenant des définitions pour tous les champs définis par l'utilisateur dans un élément Microsoft Outlook et des paramètres de liaison de données pour certains champs intégrés.</span><span class="sxs-lookup"><span data-stu-id="ca97a-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="ca97a-106">Vous pouvez manipuler la structure de flux PropertyDefinition par programmation.</span><span class="sxs-lookup"><span data-stu-id="ca97a-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="ca97a-107">Toutefois, vous pouvez obtenir des résultats similaires à l'aide du concepteur de formulaires Outlook et, en particulier, de la boîte de dialogue **Propriétés** d'un contrôle lié aux données.</span><span class="sxs-lookup"><span data-stu-id="ca97a-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="ca97a-108">Les définitions de champ dans une structure de flux PropertyDefinition peuvent être l'un des deux formats suivants: PropDefV1 et PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="ca97a-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="ca97a-109">Outlook prend en charge à la fois PropDefV1 et PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="ca97a-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="ca97a-110">Toutes les définitions de champ d'une structure de flux PropertyDefinition unique doivent être du même format.</span><span class="sxs-lookup"><span data-stu-id="ca97a-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="ca97a-111">Pour plus d'informations sur la façon dont PropDefV1 et PropDefV2 diffèrent, voir [FieldDefinition Stream structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="ca97a-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="ca97a-112">Les éléments de données dans ce flux sont stockés dans l'ordre d'octet Little-endian, immédiatement suivant l'ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ca97a-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="ca97a-113">Version: WORD (2 octets), le format des définitions de champ dans la structure de flux PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ca97a-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="ca97a-114">Le tableau suivant montre les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="ca97a-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="ca97a-115">**Value**</span><span class="sxs-lookup"><span data-stu-id="ca97a-115">**Value**</span></span>|<span data-ttu-id="ca97a-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="ca97a-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="ca97a-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="ca97a-117">0x0102</span></span>  <br/> |<span data-ttu-id="ca97a-118">Le format est PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="ca97a-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="ca97a-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="ca97a-119">0x0103</span></span>  <br/> |<span data-ttu-id="ca97a-120">Le format est PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="ca97a-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="ca97a-121">FieldDefinitionCount: DWORD (4 octets), le nombre de définitions de champ dans ce flux.</span><span class="sxs-lookup"><span data-stu-id="ca97a-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="ca97a-122">Il s'agit du nombre d'éléments de tableau dans l'élément de données FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="ca97a-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="ca97a-123">FieldDefinitions: tableau de structures de flux FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="ca97a-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="ca97a-124">Le nombre de ce tableau est égal à l'élément de données FieldDefinitionCount.</span><span class="sxs-lookup"><span data-stu-id="ca97a-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca97a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca97a-125">See also</span></span>

- [<span data-ttu-id="ca97a-126">Éléments et champs Outlook</span><span class="sxs-lookup"><span data-stu-id="ca97a-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="ca97a-127">Ajouter une définition pour un nouveau champ défini par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="ca97a-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="ca97a-128">Exemple de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="ca97a-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="ca97a-129">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="ca97a-129">Stream Structures</span></span>](stream-structures.md)

