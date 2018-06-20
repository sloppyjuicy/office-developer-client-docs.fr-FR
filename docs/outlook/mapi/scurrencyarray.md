---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787097"
---
# <a name="scurrencyarray"></a><span data-ttu-id="b2669-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="b2669-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="b2669-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2669-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2669-105">Contient un tableau de valeurs monétaires qui sont utilisées pour décrire une propriété de type PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="b2669-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2669-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b2669-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2669-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b2669-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="b2669-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b2669-108">Members</span></span>

 <span data-ttu-id="b2669-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b2669-109">**cValues**</span></span>
  
> <span data-ttu-id="b2669-110">Nombre de valeurs dans le tableau indiqué par le membre **lpcur** .</span><span class="sxs-lookup"><span data-stu-id="b2669-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="b2669-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="b2669-111">**lpcur**</span></span>
  
> <span data-ttu-id="b2669-112">Pointeur vers un tableau de structures de [devise](currency.md) qui contiennent les valeurs monétaires.</span><span class="sxs-lookup"><span data-stu-id="b2669-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2669-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2669-113">Remarks</span></span>

<span data-ttu-id="b2669-114">Pour plus d’informations sur PT_MV_CURRENCY, voir la [Liste des Types de propriété](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b2669-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2669-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2669-115">See also</span></span>



[<span data-ttu-id="b2669-116">DEVISE</span><span class="sxs-lookup"><span data-stu-id="b2669-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="b2669-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b2669-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b2669-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="b2669-118">MAPI Structures</span></span>](mapi-structures.md)

