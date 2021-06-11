---
title: Structure de flux PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422613"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="bb46e-103">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="bb46e-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="bb46e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb46e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb46e-105">La structure de flux PackedUnicodeString contient une représentation Unicode (UTF-16) d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="bb46e-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="bb46e-106">Cette chaîne n’est pas terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="bb46e-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="bb46e-107">Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="bb46e-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="bb46e-108">Les éléments de données réels qui existent dépendent de la longueur de la chaîne dans la représentation UTF-16.</span><span class="sxs-lookup"><span data-stu-id="bb46e-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="bb46e-109">Pour une chaîne dont la représentation UTF-16 contient moins de 255 WCHAR, les éléments de données sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="bb46e-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="bb46e-110">Longueur : BYTE (1 byte), longueur, en nombre de WCHAR, de la représentation UTF-16 de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="bb46e-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="bb46e-111">Caractères : tableau de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="bb46e-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="bb46e-112">Le nombre de ce tableau est égal à l’élément de données Length.</span><span class="sxs-lookup"><span data-stu-id="bb46e-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="bb46e-113">Les données du tableau sont la représentation UTF-16 de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="bb46e-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="bb46e-114">Pour une chaîne dont la représentation UTF-16 contient 255 à 65 535 WCHAR, les éléments de données sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="bb46e-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="bb46e-115">Préfixe : BYTE (1 byte), la valeur de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="bb46e-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="bb46e-116">Longueur : WORD (2 octets), longueur, en nombre de WCHAR, de la représentation UTF-16 de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="bb46e-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="bb46e-117">Caractères : tableau de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="bb46e-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="bb46e-118">Le nombre de ce tableau est égal à l’élément de données Length.</span><span class="sxs-lookup"><span data-stu-id="bb46e-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="bb46e-119">Les données du tableau sont la représentation UTF-16 de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="bb46e-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb46e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb46e-120">See also</span></span>



[<span data-ttu-id="bb46e-121">Outlook Éléments et champs</span><span class="sxs-lookup"><span data-stu-id="bb46e-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="bb46e-122">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="bb46e-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="bb46e-123">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="bb46e-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

