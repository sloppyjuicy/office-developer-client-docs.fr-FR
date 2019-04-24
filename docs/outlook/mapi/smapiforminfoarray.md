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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319172"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="47df0-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="47df0-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="47df0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47df0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47df0-105">Contient un tableau de pointeurs vers des objets d'informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="47df0-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47df0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="47df0-106">Header file:</span></span>  <br/> |<span data-ttu-id="47df0-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="47df0-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="47df0-108">Macro connexe:</span><span class="sxs-lookup"><span data-stu-id="47df0-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="47df0-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="47df0-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="47df0-110">Members</span><span class="sxs-lookup"><span data-stu-id="47df0-110">Members</span></span>

 <span data-ttu-id="47df0-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="47df0-111">**cForms**</span></span>
  
> <span data-ttu-id="47df0-112">Nombre de pointeurs dans le tableau vers lequel pointe le membre **aFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="47df0-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="47df0-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="47df0-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="47df0-114">Pointeur vers un tableau de pointeurs vers des objets d'informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="47df0-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47df0-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="47df0-115">Remarks</span></span>

<span data-ttu-id="47df0-116">La structure **SMAPIFormInfoArray** est transmise en tant que paramètre dans les méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="47df0-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="47df0-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="47df0-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="47df0-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="47df0-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="47df0-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="47df0-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="47df0-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="47df0-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="47df0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47df0-121">See also</span></span>



[<span data-ttu-id="47df0-122">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="47df0-122">MAPI Structures</span></span>](mapi-structures.md)

