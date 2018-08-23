---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 389984f9d98ece6b2040edd741e3028fd7d766ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579311"
---
# <a name="smapiformproparray"></a><span data-ttu-id="21b79-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="21b79-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="21b79-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21b79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21b79-105">Contient un tableau de structures [SMAPIFormProp](smapiformprop.md) .</span><span class="sxs-lookup"><span data-stu-id="21b79-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21b79-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="21b79-106">Header file:</span></span>  <br/> |<span data-ttu-id="21b79-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="21b79-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="21b79-108">Macro connexe :</span><span class="sxs-lookup"><span data-stu-id="21b79-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="21b79-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="21b79-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="21b79-110">Members</span><span class="sxs-lookup"><span data-stu-id="21b79-110">Members</span></span>

 <span data-ttu-id="21b79-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="21b79-111">**cProps**</span></span>
  
> <span data-ttu-id="21b79-112">Nombre de propriétés nommées dans le tableau dans le membre **aFormProp** .</span><span class="sxs-lookup"><span data-stu-id="21b79-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="21b79-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="21b79-113">**ulPad**</span></span>
  
>  <span data-ttu-id="21b79-114">Huit octets de remplissage utilisé pour garantir l’alignement correct.</span><span class="sxs-lookup"><span data-stu-id="21b79-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="21b79-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="21b79-115">**aFormProp**</span></span>
  
> <span data-ttu-id="21b79-116">Tableau de propriétés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="21b79-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21b79-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="21b79-117">Remarks</span></span>

<span data-ttu-id="21b79-118">La structure **SMAPIFormPropArray** est transmise en tant que paramètre aux méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="21b79-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="21b79-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="21b79-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="21b79-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="21b79-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="21b79-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="21b79-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="21b79-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21b79-122">See also</span></span>



[<span data-ttu-id="21b79-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="21b79-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="21b79-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="21b79-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="21b79-125">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="21b79-125">MAPI Structures</span></span>](mapi-structures.md)

