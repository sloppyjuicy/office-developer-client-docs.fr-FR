---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577680"
---
# <a name="spropattrarray"></a><span data-ttu-id="2d40c-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="2d40c-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="2d40c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d40c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d40c-105">Contient une liste d’attributs pour les propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="2d40c-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d40c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2d40c-106">Header file:</span></span>  <br/> |<span data-ttu-id="2d40c-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="2d40c-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="2d40c-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="2d40c-108">Related macros:</span></span>  <br/> |<span data-ttu-id="2d40c-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="2d40c-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="2d40c-110">Members</span><span class="sxs-lookup"><span data-stu-id="2d40c-110">Members</span></span>

 <span data-ttu-id="2d40c-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2d40c-111">**cValues**</span></span>
  
> <span data-ttu-id="2d40c-112">Nombre d’attributs de propriété dans le membre **aPropAttr** .</span><span class="sxs-lookup"><span data-stu-id="2d40c-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="2d40c-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="2d40c-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="2d40c-114">Tableau d’attributs de propriété.</span><span class="sxs-lookup"><span data-stu-id="2d40c-114">An array of property attributes.</span></span> <span data-ttu-id="2d40c-115">Les valeurs valides pour les attributs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d40c-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="2d40c-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="2d40c-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="2d40c-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="2d40c-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="2d40c-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="2d40c-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="2d40c-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="2d40c-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d40c-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d40c-120">Remarks</span></span>

<span data-ttu-id="2d40c-121">La structure **SPropAttrArray** est utilisée par les objets de données de propriété qui implémentent le [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="2d40c-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="2d40c-122">Il est également utilisé par l’implémentation de MAPI de [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) qui est en fonction de stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="2d40c-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d40c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d40c-123">See also</span></span>



[<span data-ttu-id="2d40c-124">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2d40c-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="2d40c-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d40c-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="2d40c-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="2d40c-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="2d40c-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="2d40c-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="2d40c-128">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="2d40c-128">MAPI Structures</span></span>](mapi-structures.md)

