---
title: Structures de flux de données
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6ec44fe0dbf8e63b7bbc58da1ba6e20f8ff59d3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787267"
---
# <a name="stream-structures"></a><span data-ttu-id="4a57d-103">Structures de flux de données</span><span class="sxs-lookup"><span data-stu-id="4a57d-103">Stream Structures</span></span>

  
  
<span data-ttu-id="4a57d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a57d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a57d-105">Définitions des champs définis par l’utilisateur d’un élément de Microsoft Outlook sont stockées dans la propriété [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="4a57d-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="4a57d-106">La valeur de cette propriété est un flux binaire qui contient des définitions de champs définis par l’utilisateur et les paramètres de liaison de données pour les champs intégrés pour l’élément Outlook.</span><span class="sxs-lookup"><span data-stu-id="4a57d-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="4a57d-107">Cette section fournit des informations sur la structure de l’objet stream binaire, réparti dans les structures de flux de données suivantes.</span><span class="sxs-lookup"><span data-stu-id="4a57d-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4a57d-108">Les noms de ces structures de flux de données (par exemple, la définition PropertyDefinition, FieldDefinition et SkipBlock) et leurs éléments de données ne sont pas techniquement partie de l’interface de programmation de l’API de messagerie (MAPI) et sont fournies ici uniquement pour la documentation à des fins des structures de flux de données réelles.</span><span class="sxs-lookup"><span data-stu-id="4a57d-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="4a57d-109">Les développeurs peuvent étiqueter ces éléments de données et de structures de flux dans leurs applications leur guise.</span><span class="sxs-lookup"><span data-stu-id="4a57d-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="4a57d-110">La définition PropertyDefinition flux Structure</span><span class="sxs-lookup"><span data-stu-id="4a57d-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="4a57d-111">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="4a57d-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="4a57d-112">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="4a57d-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="4a57d-113">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="4a57d-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="4a57d-114">Structure de flux PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="4a57d-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="4a57d-115">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="4a57d-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="4a57d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a57d-116">See also</span></span>



[<span data-ttu-id="4a57d-117">Les champs et les éléments outlook</span><span class="sxs-lookup"><span data-stu-id="4a57d-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="4a57d-118">Ajoutez une définition pour un nouveau champ défini par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4a57d-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="4a57d-119">Exemple de flux de la définition PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a57d-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

