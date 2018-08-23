---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d7886d08c21e8fff9aceb3437ecb6bbbd970ed7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591421"
---
# <a name="ipropdatahrsetobjaccess"></a><span data-ttu-id="128c2-103">IPropData::HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="128c2-103">IPropData::HrSetObjAccess</span></span>

  
  
<span data-ttu-id="128c2-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="128c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="128c2-105">D�finit le niveau d'acc�s de l'objet.</span><span class="sxs-lookup"><span data-stu-id="128c2-105">Sets the access level for the object.</span></span>
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="128c2-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="128c2-106">Parameters</span></span>

 <span data-ttu-id="128c2-107">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="128c2-107">_ulAccess_</span></span>
  
> <span data-ttu-id="128c2-p101">[in] Un masque de bits d'indicateurs qui sp�cifie le niveau d'acc�s de l'objet. Vous pouvez d�finir un des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="128c2-p101">[in] A bitmask of flags that specifies the object's access level. One of the following flags can be set:</span></span>
    
<span data-ttu-id="128c2-110">IPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="128c2-110">IPROP_READONLY</span></span> 
  
> <span data-ttu-id="128c2-111">D�finit le niveau d'acc�s de l'objet en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="128c2-111">Sets the object's access level to read-only.</span></span> 
    
<span data-ttu-id="128c2-112">IPROP_READWRITE</span><span class="sxs-lookup"><span data-stu-id="128c2-112">IPROP_READWRITE</span></span> 
  
> <span data-ttu-id="128c2-113">D�finit le niveau d'acc�s de l'objet en lecture/�criture.</span><span class="sxs-lookup"><span data-stu-id="128c2-113">Sets the object's access level to read/write.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="128c2-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="128c2-114">Return value</span></span>

<span data-ttu-id="128c2-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="128c2-115">S_OK</span></span> 
  
> <span data-ttu-id="128c2-116">Niveau d'acc�s de l'objet a �t� correctement d�fini.</span><span class="sxs-lookup"><span data-stu-id="128c2-116">The object's access level was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="128c2-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="128c2-117">Remarks</span></span>

<span data-ttu-id="128c2-p102">La m�thode **IPropData::HrSetObjAccess** d�finit le niveau d'acc�s pour un objet dans son int�gralit�, et non des propri�t�s individuelles. **HrSetObjAccess** peut �tre utilis� pour modifier le niveau d'acc�s �tabli lorsque l'objet a �t� cr��.</span><span class="sxs-lookup"><span data-stu-id="128c2-p102">The **IPropData::HrSetObjAccess** method sets the access level for an entire object, rather than for individual properties. **HrSetObjAccess** can be used to change the access level established when the object was created.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="128c2-120">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="128c2-120">Notes to callers</span></span>

<span data-ttu-id="128c2-p103">Pour d�finir un niveau d'acc�s sur une propri�t�, d'abord appeler **HrSetObjAccess** avec l'indicateur IPROP_READWRITE dans le param�tre  _ulAccess_ pour rendre l'objet modifiable. Puis appelez la m�thode [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , en sp�cifiant la propri�t� cible dans le tableau indiqu� par le param�tre  _lpPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="128c2-p103">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable. Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="128c2-123">Pour cr�er un objet avec des propri�t�s qui seront en lecture seule aux clients, cr�ez un objet en lecture-�criture, ajoutez les propri�t�s n�cessaires et ensuite appeler **HrSetObjAccess** pour modifier l'acc�s de l'objet en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="128c2-123">To create an object with properties that will be read-only to clients, create a read/write object, add the necessary properties, and then call **HrSetObjAccess** to change the object's access to read-only.</span></span> 
  
<span data-ttu-id="128c2-124">Vous pouvez �galement utiliser **HrSetObjAccess** pour emp�cher les clients de cr�er de nouvelles propri�t�s.</span><span class="sxs-lookup"><span data-stu-id="128c2-124">You can also use **HrSetObjAccess** to prevent clients from creating new properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="128c2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="128c2-125">See also</span></span>



[<span data-ttu-id="128c2-126">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="128c2-126">IPropData::HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md)
  
[<span data-ttu-id="128c2-127">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="128c2-127">IPropData::HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md)
  
[<span data-ttu-id="128c2-128">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="128c2-128">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

