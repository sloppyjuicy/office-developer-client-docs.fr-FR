---
title: Structure de flux PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 00791ab47cc3c6bd435d6f581e5ada53ae59d73b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569196"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="712c6-103">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="712c6-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="712c6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="712c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="712c6-105">La structure de flux PackedUnicodeString contient une représentation Unicode (UTF-16) d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="712c6-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="712c6-106">Cette chaîne n’est pas terminée par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="712c6-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="712c6-107">Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="712c6-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="712c6-108">Les éléments de données réelles qui existent dépendent de la longueur de la chaîne de représentation UTF-16.</span><span class="sxs-lookup"><span data-stu-id="712c6-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="712c6-109">Une chaîne dont la représentation UTF-16 contient moins de 255 WCHAR, les éléments de données sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="712c6-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="712c6-110">Durée : Octets (1 octet), la longueur, en nombre de WCHAR, de la représentation de la chaîne UTF-16.</span><span class="sxs-lookup"><span data-stu-id="712c6-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="712c6-111">Caractères : Tableau de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="712c6-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="712c6-112">Le nombre de ce tableau est égal à l’élément de données de longueur.</span><span class="sxs-lookup"><span data-stu-id="712c6-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="712c6-113">Les données dans le tableau sont la représentation de la chaîne UTF-16.</span><span class="sxs-lookup"><span data-stu-id="712c6-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="712c6-114">Une chaîne dont la représentation UTF-16 contient WCHAR 255 et 65535, les éléments de données sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="712c6-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="712c6-115">Préfixe : Octets (1 octet), la valeur 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="712c6-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="712c6-116">Durée : Mot (2 octets), la longueur, en nombre de WCHAR, de la représentation de la chaîne UTF-16.</span><span class="sxs-lookup"><span data-stu-id="712c6-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="712c6-117">Caractères : Tableau de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="712c6-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="712c6-118">Le nombre de ce tableau est égal à l’élément de données de longueur.</span><span class="sxs-lookup"><span data-stu-id="712c6-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="712c6-119">Les données dans le tableau sont la représentation de la chaîne UTF-16.</span><span class="sxs-lookup"><span data-stu-id="712c6-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="712c6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="712c6-120">See also</span></span>



[<span data-ttu-id="712c6-121">Champs et éléments Outlook</span><span class="sxs-lookup"><span data-stu-id="712c6-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="712c6-122">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="712c6-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="712c6-123">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="712c6-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

