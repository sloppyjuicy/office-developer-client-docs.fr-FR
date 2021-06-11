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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409502"
---
# <a name="filetime"></a><span data-ttu-id="f688a-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="f688a-103">FILETIME</span></span>

  
  
<span data-ttu-id="f688a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f688a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f688a-105">Contient une valeur de date et d’heure 64 bits non signée pour un fichier.</span><span class="sxs-lookup"><span data-stu-id="f688a-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="f688a-106">Cette valeur représente le nombre d’unités de 100 nanosecondes depuis le début du 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="f688a-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f688a-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f688a-107">Header file:</span></span>  <br/> |<span data-ttu-id="f688a-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f688a-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="f688a-109">Members</span><span class="sxs-lookup"><span data-stu-id="f688a-109">Members</span></span>

 <span data-ttu-id="f688a-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="f688a-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="f688a-111">32 bits de faible ordre de la valeur de temps du fichier.</span><span class="sxs-lookup"><span data-stu-id="f688a-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="f688a-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="f688a-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="f688a-113">Ordre élevé de 32 bits de la valeur de temps du fichier.</span><span class="sxs-lookup"><span data-stu-id="f688a-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f688a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f688a-114">Remarks</span></span>

<span data-ttu-id="f688a-115">Une propriété de type PT_SYSTIME a une structure **FILETIME** pour sa valeur.</span><span class="sxs-lookup"><span data-stu-id="f688a-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="f688a-116">Une telle propriété possède un type **de données FILETIME** pour le membre **Value** dans sa définition dans une structure [SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="f688a-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="f688a-117">La définition de la structure **FILETIME** se trouve dans la référence du programmeur  _Win32_ et dans le fichier d’en-tête MAPI Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="f688a-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="f688a-118">MAPI définit la structure de manière conditionnelle pour s’assurer qu’elle est définie lorsque la définition Win32 n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="f688a-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f688a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f688a-119">See also</span></span>



[<span data-ttu-id="f688a-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f688a-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f688a-121">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="f688a-121">MAPI Structures</span></span>](mapi-structures.md)

