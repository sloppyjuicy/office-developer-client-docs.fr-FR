---
title: PackedAnsiString Stream Structure
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404504"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="49de9-103">PackedAnsiString Stream Structure</span><span class="sxs-lookup"><span data-stu-id="49de9-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="49de9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49de9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49de9-105">La structure de flux PackedAnsiString contient une représentation ANSI d’une chaîne, basée sur la page de code ANSI de l’ordinateur sur lequel Microsoft Outlook est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="49de9-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="49de9-106">Cette chaîne n’est pas terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="49de9-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="49de9-107">Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="49de9-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="49de9-108">Les éléments de données réels qui existent dépendent de la longueur de la chaîne dans la représentation ANSI.</span><span class="sxs-lookup"><span data-stu-id="49de9-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="49de9-109">Pour une chaîne dont la représentation ANSI contient moins de 255 octets, les éléments de données sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="49de9-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="49de9-110">Longueur : BYTE (1 octet), longueur, en nombre d’octets, de la représentation ANSI de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="49de9-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="49de9-111">Characters: An array of CHAR.</span><span class="sxs-lookup"><span data-stu-id="49de9-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="49de9-112">Le nombre de ce tableau est égal à l’élément de données Length.</span><span class="sxs-lookup"><span data-stu-id="49de9-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="49de9-113">Les données du tableau sont la représentation ANSI de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="49de9-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="49de9-114">Pour une chaîne dont la représentation ANSI contient entre 255 et 65 535 octets, les éléments de données sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="49de9-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="49de9-115">Préfixe : BYTE (1 byte), la valeur de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="49de9-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="49de9-116">Longueur : WORD (2 octets), longueur, en nombre d’octets, de la représentation ANSI de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="49de9-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="49de9-117">Characters: An array of CHAR.</span><span class="sxs-lookup"><span data-stu-id="49de9-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="49de9-118">Le nombre de ce tableau est égal à l’élément de données Length.</span><span class="sxs-lookup"><span data-stu-id="49de9-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="49de9-119">Les données du tableau sont la représentation ANSI de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="49de9-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49de9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49de9-120">See also</span></span>



[<span data-ttu-id="49de9-121">Outlook Éléments et champs</span><span class="sxs-lookup"><span data-stu-id="49de9-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="49de9-122">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="49de9-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="49de9-123">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="49de9-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

