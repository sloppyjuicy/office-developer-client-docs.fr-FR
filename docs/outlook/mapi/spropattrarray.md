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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e9ad675e6df88265238a28f18e5cfcdacfdfbb5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787231"
---
# <a name="spropattrarray"></a><span data-ttu-id="aacb3-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="aacb3-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="aacb3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aacb3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aacb3-105">Contient une liste d’attributs pour les propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="aacb3-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aacb3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="aacb3-106">Header file:</span></span>  <br/> |<span data-ttu-id="aacb3-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="aacb3-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="aacb3-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="aacb3-108">Related macros:</span></span>  <br/> |<span data-ttu-id="aacb3-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="aacb3-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="aacb3-110">Membres</span><span class="sxs-lookup"><span data-stu-id="aacb3-110">Members</span></span>

 <span data-ttu-id="aacb3-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="aacb3-111">**cValues**</span></span>
  
> <span data-ttu-id="aacb3-112">Nombre d’attributs de propriété dans le membre **aPropAttr** .</span><span class="sxs-lookup"><span data-stu-id="aacb3-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="aacb3-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="aacb3-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="aacb3-114">Tableau d’attributs de propriété.</span><span class="sxs-lookup"><span data-stu-id="aacb3-114">An array of property attributes.</span></span> <span data-ttu-id="aacb3-115">Les valeurs valides pour les attributs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="aacb3-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="aacb3-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="aacb3-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="aacb3-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="aacb3-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="aacb3-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="aacb3-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="aacb3-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="aacb3-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aacb3-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="aacb3-120">Remarks</span></span>

<span data-ttu-id="aacb3-121">La structure **SPropAttrArray** est utilisée par les objets de données de propriété qui implémentent le [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="aacb3-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="aacb3-122">Il est également utilisé par l’implémentation de MAPI de [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) qui est en fonction de stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="aacb3-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aacb3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aacb3-123">See also</span></span>



[<span data-ttu-id="aacb3-124">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aacb3-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="aacb3-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aacb3-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="aacb3-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="aacb3-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="aacb3-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="aacb3-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="aacb3-128">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="aacb3-128">MAPI Structures</span></span>](mapi-structures.md)

