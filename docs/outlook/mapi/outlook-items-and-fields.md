---
title: Les champs et les éléments outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 71c67c37cc4f9cd3ddd7a55c37c4ebd6ddd35cfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784952"
---
# <a name="outlook-items-and-fields"></a><span data-ttu-id="8408e-103">Les champs et les éléments outlook</span><span class="sxs-lookup"><span data-stu-id="8408e-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="8408e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8408e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8408e-105">Microsoft Outlook fournit des types d’éléments qui sont spécialisés pour leurs fonctionnalités (par exemple, éléments de courrier, rendez-vous, contacts, tâches et notes).</span><span class="sxs-lookup"><span data-stu-id="8408e-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="8408e-106">Outlook fournit des champs standard pour chaque type d’élément, souvent appelée champs intégrés.</span><span class="sxs-lookup"><span data-stu-id="8408e-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="8408e-107">Outlook permet également aux utilisateurs de créer des champs personnalisés, communément appelé champs définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8408e-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="8408e-108">Chaque champ est associé à un type de données et une valeur.</span><span class="sxs-lookup"><span data-stu-id="8408e-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="8408e-109">**Devise**, **Date/heure**, **durée**, **entier**, **mots clés**et le **texte**sont des exemples de types de données.</span><span class="sxs-lookup"><span data-stu-id="8408e-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="8408e-110">Les utilisateurs peuvent définir des champs personnalisés à l’aide du Concepteur de formulaires dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="8408e-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="8408e-111">Au niveau de la programmabilité, chaque élément est représenté par un objet [IMessage](imessageimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="8408e-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="8408e-112">Chaque champ défini par l’utilisateur est associé à une définition de champ et une valeur.</span><span class="sxs-lookup"><span data-stu-id="8408e-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="8408e-113">Définition de champ</span><span class="sxs-lookup"><span data-stu-id="8408e-113">Field Definition</span></span>

<span data-ttu-id="8408e-114">Une définition de champ inclut le nom du type de données et autres informations sur le champ.</span><span class="sxs-lookup"><span data-stu-id="8408e-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="8408e-115">Pour chaque élément, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) de l’objet **IMessage** correspondant.</span><span class="sxs-lookup"><span data-stu-id="8408e-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="8408e-116">La propriété **PidLidPropertyDefinitionStream** contient un flux binaire appelé [la définition PropertyDefinition](propertydefinition-stream-structure.md) qui contient les définitions de champ.</span><span class="sxs-lookup"><span data-stu-id="8408e-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="8408e-117">Pour plus d’informations sur les structures de flux de données pour les définitions de champ, voir [Les Structures de flux de données](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="8408e-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="8408e-118">Valeur de champ</span><span class="sxs-lookup"><span data-stu-id="8408e-118">Field Value</span></span>

<span data-ttu-id="8408e-119">Chaque champ défini par l’utilisateur d’un élément a une valeur qui est stockée dans une propriété nommée correspondante.</span><span class="sxs-lookup"><span data-stu-id="8408e-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="8408e-120">Que la propriété nommée se trouve dans le jeu de propriétés PS_PUBLIC_STRINGS et a une chaîne de caractères Unicode comme nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="8408e-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="8408e-121">Le type de données de la propriété correspond au type du champ.</span><span class="sxs-lookup"><span data-stu-id="8408e-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="8408e-122">Si la propriété n’est pas présente dans l’objet **IMessage** , Outlook suppose une valeur par défaut de la propriété.</span><span class="sxs-lookup"><span data-stu-id="8408e-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="8408e-123">Par exemple, pour un type de chaîne, Outlook suppose une chaîne vide si la propriété n’est pas présente.</span><span class="sxs-lookup"><span data-stu-id="8408e-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8408e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8408e-124">See also</span></span>



[<span data-ttu-id="8408e-125">Ajoutez une définition pour un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="8408e-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="8408e-126">Exemple de flux de la définition PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="8408e-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="8408e-127">Structures de flux de données</span><span class="sxs-lookup"><span data-stu-id="8408e-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="8408e-128">La définition PropertyDefinition flux Structure</span><span class="sxs-lookup"><span data-stu-id="8408e-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="8408e-129">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="8408e-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="8408e-130">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="8408e-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="8408e-131">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="8408e-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="8408e-132">Structure de flux PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="8408e-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="8408e-133">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="8408e-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

