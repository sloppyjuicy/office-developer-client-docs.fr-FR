---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416971"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="9d3b5-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="9d3b5-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="9d3b5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d3b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d3b5-105">Contient un tableau de pointeurs vers des objets d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="9d3b5-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d3b5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9d3b5-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d3b5-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="9d3b5-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9d3b5-108">Macro associée :</span><span class="sxs-lookup"><span data-stu-id="9d3b5-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="9d3b5-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="9d3b5-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="9d3b5-110">Members</span><span class="sxs-lookup"><span data-stu-id="9d3b5-110">Members</span></span>

 <span data-ttu-id="9d3b5-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="9d3b5-111">**cForms**</span></span>
  
> <span data-ttu-id="9d3b5-112">Nombre de pointeurs dans le tableau pointés par le **membre aFormInfo.**</span><span class="sxs-lookup"><span data-stu-id="9d3b5-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="9d3b5-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="9d3b5-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="9d3b5-114">Pointeur vers un tableau de pointeurs vers des objets d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="9d3b5-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d3b5-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d3b5-115">Remarks</span></span>

<span data-ttu-id="9d3b5-116">La structure **SMAPIFormInfoArray** est passée en tant que paramètre dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d3b5-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="9d3b5-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="9d3b5-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="9d3b5-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="9d3b5-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="9d3b5-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="9d3b5-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="9d3b5-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="9d3b5-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="9d3b5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d3b5-121">See also</span></span>



[<span data-ttu-id="9d3b5-122">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="9d3b5-122">MAPI Structures</span></span>](mapi-structures.md)

