---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a5f950907e2b14cb4101a094715c24b25beb2016
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783309"
---
# <a name="filetime"></a><span data-ttu-id="dc926-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="dc926-103">FILETIME</span></span>

  
  
<span data-ttu-id="dc926-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc926-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc926-105">Contient une date de 64 bits non signé et d’une valeur d’heure d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="dc926-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="dc926-106">Cette valeur représente le nombre d’unités de 100 nanosecondes depuis le début du 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="dc926-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc926-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dc926-107">Header file:</span></span>  <br/> |<span data-ttu-id="dc926-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc926-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="dc926-109">Membres</span><span class="sxs-lookup"><span data-stu-id="dc926-109">Members</span></span>

 <span data-ttu-id="dc926-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="dc926-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="dc926-111">Valeur de temps 32 bits de poids faible du fichier.</span><span class="sxs-lookup"><span data-stu-id="dc926-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="dc926-112">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="dc926-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="dc926-113">Ordre haut 32 bits de la valeur d’heure de fichier.</span><span class="sxs-lookup"><span data-stu-id="dc926-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc926-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="dc926-114">Remarks</span></span>

<span data-ttu-id="dc926-115">Une propriété de type PT_SYSTIME possède une structure **FILETIME** pour sa valeur.</span><span class="sxs-lookup"><span data-stu-id="dc926-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="dc926-116">Ces propriétés a un type de données **FILETIME** pour le membre de la **valeur** de sa définition dans une structure [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="dc926-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="dc926-117">La définition de la structure **FILETIME** est dans la _référence du programmeur Win32_ et dans le fichier d’en-tête Mapidefs.h MAPI.</span><span class="sxs-lookup"><span data-stu-id="dc926-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="dc926-118">MAPI définit la structure conditionnelle pour vous assurer qu’elle est définie lorsque la définition de Win32 n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="dc926-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc926-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc926-119">See also</span></span>



[<span data-ttu-id="dc926-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dc926-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="dc926-121">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="dc926-121">MAPI Structures</span></span>](mapi-structures.md)

