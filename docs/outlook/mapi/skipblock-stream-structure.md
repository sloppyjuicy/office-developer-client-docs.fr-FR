---
title: Structure de flux SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282669"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="a4fae-103">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="a4fae-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="a4fae-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4fae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4fae-105">Une structure de flux SkipBlock est un bloc de données qui commence par un entier qui spécifie la longueur de la partie restante du bloc.</span><span class="sxs-lookup"><span data-stu-id="a4fae-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="a4fae-106">Cette structure de flux existe dans un flux [FieldDefinition](fielddefinition-stream-structure.md) si la définition de champ est au format PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="a4fae-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="a4fae-107">L'objectif d'une structure de flux SkipBlock dépend de son emplacement relatif dans une série de structures similaires dans l'élément de données SkipBlocks d'un flux de FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="a4fae-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="a4fae-108">La série SkipBlocks doit contenir au moins une structure SkipBlock qui termine la série et dont l'élément de données de taille est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="a4fae-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="a4fae-109">Si la première structure n'est pas la structure de terminaison (autrement dit, l'élément de données de taille est supérieur à 0), Outlook suppose que la première structure spécifie le nom du champ en Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="a4fae-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="a4fae-110">Les éléments de données dans ce flux sont stockés dans l'ordre d'octet Little-endian, immédiatement suivant l'ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a4fae-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="a4fae-111">Size: DWORD (4 octets), taille, en nombre d'octets, de l'élément de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="a4fae-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="a4fae-112">Content: tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="a4fae-112">Content: An array of BYTE.</span></span> <span data-ttu-id="a4fae-113">Le nombre de ce tableau est égal à l'élément de données Size.</span><span class="sxs-lookup"><span data-stu-id="a4fae-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="a4fae-114">La signification de l'élément de données de contenu dépend de l'emplacement de la structure SkipBlock dans la série et de la version d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="a4fae-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="a4fae-115">Si la première structure SkipBlock n'est pas la structure de terminaison, Outlook considère la première structure SkipBlock comme la structure de flux de [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) qui spécifie le nom de champ en Unicode.</span><span class="sxs-lookup"><span data-stu-id="a4fae-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a4fae-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4fae-116">See also</span></span>



[<span data-ttu-id="a4fae-117">Éléments et champs Outlook</span><span class="sxs-lookup"><span data-stu-id="a4fae-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="a4fae-118">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="a4fae-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="a4fae-119">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="a4fae-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="a4fae-120">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="a4fae-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

