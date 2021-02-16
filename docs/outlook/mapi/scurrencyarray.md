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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439400"
---
# <a name="scurrencyarray"></a><span data-ttu-id="cd133-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="cd133-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="cd133-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd133-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd133-105">Contient un tableau de valeurs monétaires utilisées pour décrire une propriété de type PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="cd133-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd133-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="cd133-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd133-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd133-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="cd133-108">Members</span><span class="sxs-lookup"><span data-stu-id="cd133-108">Members</span></span>

 <span data-ttu-id="cd133-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="cd133-109">**cValues**</span></span>
  
> <span data-ttu-id="cd133-110">Nombre de valeurs dans le tableau pointées par **le membre lpcur.**</span><span class="sxs-lookup"><span data-stu-id="cd133-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="cd133-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="cd133-111">**lpcur**</span></span>
  
> <span data-ttu-id="cd133-112">Pointeur vers un tableau de structures [CURRENCY](currency.md) qui contiennent les valeurs monétaires.</span><span class="sxs-lookup"><span data-stu-id="cd133-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cd133-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd133-113">Remarks</span></span>

<span data-ttu-id="cd133-114">Pour plus d’informations PT_MV_CURRENCY, voir [Liste des types de propriétés.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="cd133-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd133-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd133-115">See also</span></span>



[<span data-ttu-id="cd133-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="cd133-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="cd133-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="cd133-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="cd133-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="cd133-118">MAPI Structures</span></span>](mapi-structures.md)

