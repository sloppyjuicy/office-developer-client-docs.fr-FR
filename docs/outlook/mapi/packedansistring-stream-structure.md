---
title: Structure de flux PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5494558db65e19891848264c170ba85a55c5df71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784953"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="230a2-103">Structure de flux PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="230a2-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="230a2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="230a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="230a2-105">La structure de flux PackedAnsiString contient une représentation ANSI d’une chaîne, en fonction de la page de codes ANSI de l’ordinateur sur lequel Microsoft Outlook est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="230a2-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="230a2-106">Cette chaîne n’est pas terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="230a2-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="230a2-107">Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="230a2-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="230a2-108">Les éléments de données réelles qui existent dépendent de la longueur de la chaîne de représentation ANSI.</span><span class="sxs-lookup"><span data-stu-id="230a2-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="230a2-109">Une chaîne dont la représentation ANSI contient moins de 255 octets, les éléments de données sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="230a2-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="230a2-110">Durée : Octets (1 octet), la longueur, en octets, de la représentation de la chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="230a2-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="230a2-111">Caractères : Un tableau de CHAR.</span><span class="sxs-lookup"><span data-stu-id="230a2-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="230a2-112">Le nombre de ce tableau est égal à l’élément de données de longueur.</span><span class="sxs-lookup"><span data-stu-id="230a2-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="230a2-113">Les données dans le tableau sont la représentation de la chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="230a2-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="230a2-114">Une chaîne dont la représentation ANSI contient 255 et 65535 octets, les éléments de données sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="230a2-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="230a2-115">Préfixe : Octets (1 octet), la valeur 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="230a2-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="230a2-116">Durée : Mot (2 octets), la longueur, en octets, de la représentation de la chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="230a2-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="230a2-117">Caractères : Un tableau de CHAR.</span><span class="sxs-lookup"><span data-stu-id="230a2-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="230a2-118">Le nombre de ce tableau est égal à l’élément de données de longueur.</span><span class="sxs-lookup"><span data-stu-id="230a2-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="230a2-119">Les données dans le tableau sont la représentation de la chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="230a2-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="230a2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="230a2-120">See also</span></span>



[<span data-ttu-id="230a2-121">Les champs et les éléments outlook</span><span class="sxs-lookup"><span data-stu-id="230a2-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="230a2-122">Structures de flux de données</span><span class="sxs-lookup"><span data-stu-id="230a2-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="230a2-123">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="230a2-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

