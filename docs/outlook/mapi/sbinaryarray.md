---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787048"
---
# <a name="sbinaryarray"></a><span data-ttu-id="3b5a2-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="3b5a2-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="3b5a2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b5a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b5a2-105">Contient un tableau de valeurs binaires.</span><span class="sxs-lookup"><span data-stu-id="3b5a2-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b5a2-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3b5a2-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b5a2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b5a2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="3b5a2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3b5a2-108">Members</span></span>

 <span data-ttu-id="3b5a2-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3b5a2-109">**cValues**</span></span>
  
> <span data-ttu-id="3b5a2-110">Nombre de valeurs dans le tableau indiqué par le membre **lpbin** .</span><span class="sxs-lookup"><span data-stu-id="3b5a2-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="3b5a2-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="3b5a2-111">**lpbin**</span></span>
  
> <span data-ttu-id="3b5a2-112">Pointeur vers un tableau de structures [SBinary](sbinary.md) qui contient les valeurs binaires.</span><span class="sxs-lookup"><span data-stu-id="3b5a2-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3b5a2-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b5a2-113">Remarks</span></span>

<span data-ttu-id="3b5a2-114">La structure **SBinaryArray** est utilisée pour décrire les propriétés de type PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="3b5a2-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="3b5a2-115">Pour plus d’informations sur PT_MV_BINARY, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="3b5a2-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3b5a2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b5a2-116">See also</span></span>



[<span data-ttu-id="3b5a2-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="3b5a2-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="3b5a2-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3b5a2-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3b5a2-119">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="3b5a2-119">MAPI Structures</span></span>](mapi-structures.md)

