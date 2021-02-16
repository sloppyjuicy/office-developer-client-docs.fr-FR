---
title: Structures de flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407822"
---
# <a name="stream-structures"></a><span data-ttu-id="5e4c8-103">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="5e4c8-103">Stream Structures</span></span>

  
  
<span data-ttu-id="5e4c8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e4c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e4c8-105">Les définitions des champs définis par l’utilisateur d’un élément Microsoft Outlook sont stockées dans la [propriété PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5e4c8-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="5e4c8-106">La valeur de cette propriété est un flux binaire qui contient des définitions de champs définis par l’utilisateur et des paramètres de liaison de données pour les champs intégrés pour l’élément Outlook.</span><span class="sxs-lookup"><span data-stu-id="5e4c8-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="5e4c8-107">Cette section fournit des informations sur la structure du flux binaire, décomposée dans les structures de flux suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e4c8-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5e4c8-108">Les noms de ces structures de flux (par exemple, PropertyDefinition, FieldDefinition et SkipBlock) et leurs éléments de données ne font techniquement pas partie de l’interface de programmation de l’API de messagerie (MAPI) et sont fournis ici uniquement à des fins de documentation des structures de flux réelles.</span><span class="sxs-lookup"><span data-stu-id="5e4c8-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="5e4c8-109">Les développeurs peuvent étiqueter ces structures de flux et éléments de données dans leurs applications comme ils le souhaitent.</span><span class="sxs-lookup"><span data-stu-id="5e4c8-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="5e4c8-110">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="5e4c8-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="5e4c8-111">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="5e4c8-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="5e4c8-112">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="5e4c8-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="5e4c8-113">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="5e4c8-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="5e4c8-114">PackedAnsiString Stream Structure</span><span class="sxs-lookup"><span data-stu-id="5e4c8-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="5e4c8-115">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="5e4c8-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="5e4c8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e4c8-116">See also</span></span>



[<span data-ttu-id="5e4c8-117">Éléments et champs Outlook</span><span class="sxs-lookup"><span data-stu-id="5e4c8-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="5e4c8-118">Ajouter une définition pour un nouveau champ User-Defined de recherche</span><span class="sxs-lookup"><span data-stu-id="5e4c8-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="5e4c8-119">Exemple de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="5e4c8-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

