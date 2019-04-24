---
title: Ajout de la définition d’un nouveau champ défini par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299068"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="1be2c-103">Ajout de la définition d’un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1be2c-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="1be2c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1be2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1be2c-105">Lorsque vous ajoutez un champ défini par l'utilisateur à un élément Microsoft Outlook, vous ajoutez une définition de champ à la structure de flux [PropertyDefinition](propertydefinition-stream-structure.md) correspondante.</span><span class="sxs-lookup"><span data-stu-id="1be2c-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="1be2c-106">Utilisez la procédure suivante pour ajouter une nouvelle définition de champ à une structure de flux PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1be2c-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="1be2c-107">Pour ajouter une définition pour un nouveau champ défini par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="1be2c-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="1be2c-108">Copiez les définitions de champ existantes de la structure de flux PropertyDefinition vers un nouveau tableau de définitions de champs.</span><span class="sxs-lookup"><span data-stu-id="1be2c-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="1be2c-109">Si des définitions de champ existantes sont au format PropDefV1, convertissez-les au format PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="1be2c-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="1be2c-110">Pour plus d'informations sur les formats de définition de champ, voir [PropertyDefinition Stream structure](propertydefinition-stream-structure.md) et [FieldDefinition Stream structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="1be2c-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="1be2c-111">Créez une définition du nouveau champ défini par l'utilisateur au format PropDefV2 et ajoutez-le au tableau.</span><span class="sxs-lookup"><span data-stu-id="1be2c-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="1be2c-112">Définissez l'élément version de la structure de flux PropertyDefinition en tant que 0x0103, si la valeur de l'élément version n'a pas été définie.</span><span class="sxs-lookup"><span data-stu-id="1be2c-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="1be2c-113">Incrémentez l'élément FieldDefinitionCount de 1.</span><span class="sxs-lookup"><span data-stu-id="1be2c-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="1be2c-114">Stockez le tableau en tant que valeur de l'élément FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="1be2c-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1be2c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1be2c-115">See also</span></span>

- [<span data-ttu-id="1be2c-116">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="1be2c-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

