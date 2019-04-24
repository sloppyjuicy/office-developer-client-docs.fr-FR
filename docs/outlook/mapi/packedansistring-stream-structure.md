---
title: Structure de flux PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348509"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="4f74c-103">Structure de flux PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="4f74c-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="4f74c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f74c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f74c-105">La structure de flux PackedAnsiString contient une représentation ANSI d'une chaîne, basée sur la page de code ANSI de l'ordinateur sur lequel Microsoft Outlook est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="4f74c-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="4f74c-106">Cette chaîne n'est pas terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="4f74c-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="4f74c-107">Les éléments de données dans ce flux sont stockés dans l'ordre d'octet Little-endian, immédiatement suivant l'ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4f74c-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="4f74c-108">Les éléments de données réels qui existent dépendent de la longueur de la chaîne en représentation ANSI.</span><span class="sxs-lookup"><span data-stu-id="4f74c-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="4f74c-109">Pour une chaîne dont la représentation ANSI contient moins de 255 octets, les éléments de données sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="4f74c-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="4f74c-110">Length: octet (1 octet), longueur, en nombre d'octets, de la représentation ANSI de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="4f74c-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="4f74c-111">Caractères: tableau de CHAR.</span><span class="sxs-lookup"><span data-stu-id="4f74c-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="4f74c-112">Le décompte de ce tableau est égal à l'élément de données length.</span><span class="sxs-lookup"><span data-stu-id="4f74c-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="4f74c-113">Les données dans le tableau sont la représentation ANSI de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="4f74c-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="4f74c-114">Pour une chaîne dont la représentation ANSI contient 255 à 65535 octets, les éléments de données sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="4f74c-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="4f74c-115">PréFixe: octet (1 octet), valeur de 255 (0xFF).</span><span class="sxs-lookup"><span data-stu-id="4f74c-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="4f74c-116">Length: WORD (2 octets), longueur, en nombre d'octets, de la représentation ANSI de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="4f74c-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="4f74c-117">Caractères: tableau de CHAR.</span><span class="sxs-lookup"><span data-stu-id="4f74c-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="4f74c-118">Le décompte de ce tableau est égal à l'élément de données length.</span><span class="sxs-lookup"><span data-stu-id="4f74c-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="4f74c-119">Les données dans le tableau sont la représentation ANSI de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="4f74c-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f74c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f74c-120">See also</span></span>



[<span data-ttu-id="4f74c-121">Éléments et champs Outlook</span><span class="sxs-lookup"><span data-stu-id="4f74c-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="4f74c-122">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="4f74c-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="4f74c-123">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="4f74c-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

