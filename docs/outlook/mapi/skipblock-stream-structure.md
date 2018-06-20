---
title: Structure de flux SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d84704300602bada4cf93c9d3f6622feaf16f352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787185"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="1069c-103">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="1069c-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="1069c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1069c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1069c-105">Une structure de flux SkipBlock est un bloc de données qui commence par un entier qui spécifie la longueur de la partie restante du bloc.</span><span class="sxs-lookup"><span data-stu-id="1069c-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="1069c-106">Cette structure de flux de données existe dans un flux [FieldDefinition](fielddefinition-stream-structure.md) si la définition de champ est au format PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="1069c-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="1069c-107">L’objectif d’une structure de flux SkipBlock dépend de son emplacement relatif dans une série de comme les structures dans l’élément de données SkipBlocks d’un flux FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="1069c-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="1069c-108">La série SkipBlocks doit contenir au moins une structure SkipBlock qui met fin à la série et comporte l’élément de données de taille égale à 0.</span><span class="sxs-lookup"><span data-stu-id="1069c-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="1069c-109">Si la première structure n’est pas la structure de fin (autrement dit, l’élément de données de taille est supérieure à 0), Outlook suppose que la première structure Spécifie le nom de champ en Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="1069c-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="1069c-110">Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1069c-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="1069c-111">Taille : DWORD (4 octets), la taille, en octets, de l’élément de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="1069c-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="1069c-112">Contenu : Un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="1069c-112">Content: An array of BYTE.</span></span> <span data-ttu-id="1069c-113">Le nombre de ce tableau est égal à l’élément de données de taille.</span><span class="sxs-lookup"><span data-stu-id="1069c-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="1069c-114">La signification de l’élément de données de contenu dépend de l’emplacement de la structure SkipBlock dans la série et la version d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="1069c-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="1069c-115">Si la première structure SkipBlock n’est pas la structure rencontrée, Outlook considère que la première structure SkipBlock que la structure de flux [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) qui spécifie le nom de champ en Unicode.</span><span class="sxs-lookup"><span data-stu-id="1069c-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1069c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1069c-116">See also</span></span>



[<span data-ttu-id="1069c-117">Les champs et les éléments outlook</span><span class="sxs-lookup"><span data-stu-id="1069c-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="1069c-118">Structures de flux de données</span><span class="sxs-lookup"><span data-stu-id="1069c-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="1069c-119">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="1069c-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="1069c-120">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="1069c-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

