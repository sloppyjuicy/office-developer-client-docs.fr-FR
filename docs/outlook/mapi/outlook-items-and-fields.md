---
title: Outlook Éléments et champs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409117"
---
# <a name="outlook-items-and-fields"></a><span data-ttu-id="16cb2-103">Outlook Éléments et champs</span><span class="sxs-lookup"><span data-stu-id="16cb2-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="16cb2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16cb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16cb2-105">Microsoft Outlook fournit des types d’éléments spécialisés pour leurs fonctionnalités (par exemple, éléments de courrier, rendez-vous, contacts, tâches et notes).</span><span class="sxs-lookup"><span data-stu-id="16cb2-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="16cb2-106">Outlook fournit des champs standard pour chaque type d’élément, communément appelés champs intégrés.</span><span class="sxs-lookup"><span data-stu-id="16cb2-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="16cb2-107">Outlook permet également aux utilisateurs de créer des champs personnalisés, communément appelés champs définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16cb2-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="16cb2-108">Chaque champ est associé à un type de données et à une valeur.</span><span class="sxs-lookup"><span data-stu-id="16cb2-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="16cb2-109">Exemples de types de données **sont Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords** et **Text**.</span><span class="sxs-lookup"><span data-stu-id="16cb2-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="16cb2-110">Les utilisateurs peuvent définir des champs personnalisés à l’aide du Concepteur de formulaires dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="16cb2-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="16cb2-111">Au niveau de la programmabilité, chaque élément est représenté par un [objet IMessage.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="16cb2-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="16cb2-112">Chaque champ défini par l’utilisateur est associé à une définition de champ et à une valeur.</span><span class="sxs-lookup"><span data-stu-id="16cb2-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="16cb2-113">Définition de champ</span><span class="sxs-lookup"><span data-stu-id="16cb2-113">Field Definition</span></span>

<span data-ttu-id="16cb2-114">Une définition de champ inclut le nom, le type de données et d’autres informations sur le champ.</span><span class="sxs-lookup"><span data-stu-id="16cb2-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="16cb2-115">Pour chaque élément, Outlook stocke les définitions de tous les champs définis par l’utilisateur dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) de l’objet **IMessage** correspondant.</span><span class="sxs-lookup"><span data-stu-id="16cb2-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="16cb2-116">La **propriété PidLidPropertyDefinitionStream** contient un flux binaire appelé [PropertyDefinition](propertydefinition-stream-structure.md) qui contient les définitions de champ.</span><span class="sxs-lookup"><span data-stu-id="16cb2-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="16cb2-117">Pour plus d’informations sur les structures de flux pour les définitions de champ, voir [Stream Structures](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="16cb2-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="16cb2-118">Valeur de champ</span><span class="sxs-lookup"><span data-stu-id="16cb2-118">Field Value</span></span>

<span data-ttu-id="16cb2-119">Chaque champ défini par l’utilisateur d’un élément possède une valeur stockée dans une propriété nommée correspondante.</span><span class="sxs-lookup"><span data-stu-id="16cb2-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="16cb2-120">Cette propriété nommée se trouve dans le jeu de PS_PUBLIC_STRINGS et possède une chaîne de caractères Unicode comme nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="16cb2-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="16cb2-121">Le type de données de la propriété correspond au type du champ.</span><span class="sxs-lookup"><span data-stu-id="16cb2-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="16cb2-122">Si la propriété n’est pas présente dans l’objet **IMessage,** Outlook une valeur par défaut raisonnable pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="16cb2-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="16cb2-123">Par exemple, pour un type de chaîne, Outlook une chaîne vide si la propriété n’est pas présente.</span><span class="sxs-lookup"><span data-stu-id="16cb2-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16cb2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16cb2-124">See also</span></span>



[<span data-ttu-id="16cb2-125">Ajouter une définition pour un nouveau champ User-Defined de recherche</span><span class="sxs-lookup"><span data-stu-id="16cb2-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="16cb2-126">Exemple de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="16cb2-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="16cb2-127">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="16cb2-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="16cb2-128">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="16cb2-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="16cb2-129">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="16cb2-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="16cb2-130">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="16cb2-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="16cb2-131">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="16cb2-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="16cb2-132">PackedAnsiString Stream Structure</span><span class="sxs-lookup"><span data-stu-id="16cb2-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="16cb2-133">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="16cb2-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

