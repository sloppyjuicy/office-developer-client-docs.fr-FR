---
title: Ajout de la définition d’un nouveau champ défini par l’utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428164"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="fe791-103">Ajout de la définition d’un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fe791-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="fe791-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe791-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe791-105">Lorsque vous ajoutez un champ défini par l’utilisateur à un élément Microsoft Outlook, vous ajoutez une définition de champ à la structure de flux [PropertyDefinition](propertydefinition-stream-structure.md) correspondante.</span><span class="sxs-lookup"><span data-stu-id="fe791-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="fe791-106">Utilisez la procédure suivante pour ajouter une nouvelle définition de champ à une structure de flux PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="fe791-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="fe791-107">Pour ajouter une définition pour un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="fe791-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="fe791-108">Copiez les définitions de champ existantes de la structure de flux PropertyDefinition dans un nouveau tableau de définitions de champs.</span><span class="sxs-lookup"><span data-stu-id="fe791-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="fe791-109">Si des définitions de champ existantes sont au format PropDefV1, convertissez-les au format PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="fe791-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="fe791-110">Pour plus d’informations sur les formats de définition de champ, voir [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) et [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="fe791-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="fe791-111">Créez une définition du nouveau champ défini par l’utilisateur au format PropDefV2 et ajoutez-la au tableau.</span><span class="sxs-lookup"><span data-stu-id="fe791-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="fe791-112">Définissez l’élément Version de la structure de flux PropertyDefinition comme 0x0103, si l’élément Version n’a pas été définie sur cette valeur.</span><span class="sxs-lookup"><span data-stu-id="fe791-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="fe791-113">Incrémenter l’élément FieldDefinitionCount par 1.</span><span class="sxs-lookup"><span data-stu-id="fe791-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="fe791-114">Stockez le tableau en tant que valeur de l’élément FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="fe791-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe791-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe791-115">See also</span></span>

- [<span data-ttu-id="fe791-116">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="fe791-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

