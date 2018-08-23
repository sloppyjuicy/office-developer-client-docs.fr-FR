---
title: Ajoutez une définition pour un nouveau champ défini par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a2f9d1623c3733292ebf5c65452ac0d65f577c4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592716"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="58063-103">Ajoutez une définition pour un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="58063-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="58063-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58063-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58063-105">Lorsque vous ajoutez un champ défini par l’utilisateur à un élément Microsoft Outlook, vous ajoutez une définition de champ à la structure de flux de [la définition PropertyDefinition](propertydefinition-stream-structure.md) correspondante.</span><span class="sxs-lookup"><span data-stu-id="58063-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="58063-106">Utilisez la procédure suivante pour ajouter une nouvelle définition de champ à une structure de flux de la définition PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="58063-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="58063-107">Pour ajouter une définition pour un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="58063-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="58063-108">Copiez les définitions de champ existant de la structure de flux de la définition PropertyDefinition vers un nouveau tableau de définitions de champ.</span><span class="sxs-lookup"><span data-stu-id="58063-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="58063-109">S’il y a des définitions de champ existant dans le format PropDefV1, les convertir au format PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="58063-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="58063-110">Pour plus d’informations sur les formats de définition de champ, voir la [Structure de flux de la définition PropertyDefinition](propertydefinition-stream-structure.md) et [FieldDefinition flux](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="58063-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="58063-111">Créer une définition du nouveau champ défini par l’utilisateur dans le format PropDefV2 et l’ajouter au tableau.</span><span class="sxs-lookup"><span data-stu-id="58063-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="58063-112">Définir l’élément de la Version de la structure de flux de la définition PropertyDefinition comme 0x0103, si l’élément Version n’a pas été définie pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="58063-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="58063-113">Incrémenter l’élément FieldDefinitionCount de 1.</span><span class="sxs-lookup"><span data-stu-id="58063-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="58063-114">Stocker en tant que la valeur de l’élément FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="58063-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58063-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58063-115">See also</span></span>

- [<span data-ttu-id="58063-116">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="58063-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

