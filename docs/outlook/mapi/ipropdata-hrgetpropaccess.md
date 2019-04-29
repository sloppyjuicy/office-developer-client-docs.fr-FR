---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5e36cf12b7a5b1643f5a0ec97223030718195a7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433436"
---
# <a name="ipropdatahrgetpropaccess"></a><span data-ttu-id="a4b8f-103">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="a4b8f-103">IPropData::HrGetPropAccess</span></span>

  
  
<span data-ttu-id="a4b8f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4b8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4b8f-105">R�cup�re le niveau d'acc�s et l'�tat d'un ou plusieurs des propri�t�s de l'objet.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-105">Retrieves the access level and status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="a4b8f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4b8f-106">Parameters</span></span>

 <span data-ttu-id="a4b8f-107">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="a4b8f-107">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="a4b8f-p101">[entr�e, sortie] � l'entr�e, un tableau de balises de propri�t�s qui indiquent les propri�t�s pour lequel r�cup�rer des niveaux d'acc�s et l'�tat ; dans le cas contraire, un pointeur null, ce qui indique que **HrGetPropAccess** doit extraire les niveaux d'acc�s et l'�tat de toutes les propri�t�s. Dans la sortie, un tableau de balises de propri�t� pour les indicateurs d'acc�s et l'�tat ont �t� r�cup�r�s. Les indicateurs sont stock�s dans le tableau indiqu� par le param�tre  _lprgulAccess_.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-p101">[in, out] On input, an array of property tags that indicate the properties for which to retrieve access levels and status; otherwise, a pointer to NULL, which indicates that **HrGetPropAccess** should retrieve access levels and status for all properties. On output, an array of property tags for which access and status flags were retrieved. The flags are stored in the array pointed to by the  _lprgulAccess_ parameter.</span></span> 
    
 <span data-ttu-id="a4b8f-111">_lprgulAccess_</span><span class="sxs-lookup"><span data-stu-id="a4b8f-111">_lprgulAccess_</span></span>
  
> <span data-ttu-id="a4b8f-p102">[out] Pointeur vers un tableau de masques de bits indicateur. Chaque masque de bits indique les niveaux d'acc�s ou l'�tat ou les deux, pour chacune des propri�t�s identifi�es dans le tableau indiqu� par le param�tre  _lpPropTagArray_. Les deux tableaux sont positionnels dans la mesure o� le premier masque de bits que points  _lprgulAccess_ � d�crit la premi�re propri�t� que  _lpPropTagArray_ pointe, et ainsi de suite. Pour chaque balise de propri�t�, les indicateurs suivants peuvent �tre d�finis :</span><span class="sxs-lookup"><span data-stu-id="a4b8f-p102">[out] A pointer to an array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array pointed to by the  _lpPropTagArray_ parameter. The two arrays are positional in that the first bitmask that  _lprgulAccess_ points to describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, the following flags can be set:</span></span> 
    
|<span data-ttu-id="a4b8f-116">**Indicateur de niveau d'acc�s**</span><span class="sxs-lookup"><span data-stu-id="a4b8f-116">**Access-level flag**</span></span>|<span data-ttu-id="a4b8f-117">**Indicateur d'�tat**</span><span class="sxs-lookup"><span data-stu-id="a4b8f-117">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4b8f-118">IPROP_READONLY, ce qui indique que la propri�t� ne peut pas �tre modifi�e.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-118">IPROP_READONLY, which indicates that the property cannot be modified.</span></span>  <br/> |<span data-ttu-id="a4b8f-119">IPROP_CLEAN, ce qui indique que la propri�t� n'a pas �t� modifi�e.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-119">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="a4b8f-120">IPROP_READWRITE, ce qui indique que la propri�t� peut �tre modifi�e.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-120">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="a4b8f-121">IPROP_DIRTY, ce qui indique que la propri�t� a �t� modifi�e.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-121">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="a4b8f-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a4b8f-122">Return value</span></span>

<span data-ttu-id="a4b8f-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4b8f-123">S_OK</span></span> 
  
> <span data-ttu-id="a4b8f-124">Les indicateurs de niveau et l'�tat de l'acc�s pour les propri�t�s ont �t� renvoy�es avec succ�s.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-124">The access level and status flags for the properties were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4b8f-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4b8f-125">Remarks</span></span>

<span data-ttu-id="a4b8f-126">La m�thode **IPropData::HrGetPropAccess** r�cup�re un ensemble d'indicateurs qui indique le niveau d'acc�s et l'�tat d'une ou plusieurs propri�t�s.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-126">The **IPropData::HrGetPropAccess** method retrieves a set of flags that indicates the access level and status for one or more properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4b8f-127">Remarques aux appelants :</span><span class="sxs-lookup"><span data-stu-id="a4b8f-127">Notes to callers:</span></span>

<span data-ttu-id="a4b8f-128">Vous pouvez utiliser **HrGetPropAccess** dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="a4b8f-128">You can use **HrGetPropAccess** for the following purposes:</span></span> 
  
- <span data-ttu-id="a4b8f-129">Pour d�terminer si un client modifi� ou supprim� une propri�t� accessible en �criture.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-129">To determine whether a client changed or deleted a writable property.</span></span>
    
- <span data-ttu-id="a4b8f-130">Pour emp�cher un client � partir de la modification ou suppression d'une propri�t� en utilisant les m�thodes [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="a4b8f-130">To prevent a client from changing or deleting a property by using the [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
    
<span data-ttu-id="a4b8f-p103">Si une des propri�t�s dans le tableau de balise de propri�t� d�sign�s par  _lppPropTagArray_ a �t� supprim�e, **HrGetPropAccess** d�finit l'entr�e du tableau � 0 � la sortie. Si vous d�finissez  _lppPropTagArray_ sur NULL et une des propri�t�s de l'objet a �t� supprim�e, la propri�t� deleted est renvoy�e dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-p103">If one of the properties in the property tag array pointed to by  _lppPropTagArray_ has been deleted, **HrGetPropAccess** sets the array entry to 0 on output. If you set  _lppPropTagArray_ to NULL and one of the object's properties has been deleted, the deleted property is returned in the array.</span></span> 
  
<span data-ttu-id="a4b8f-p104">Si une propri�t� a �t� modifi�e, son indicateur IPROP_DIRTY est d�fini dans l'entr�e correspondante dans le tableau qui pointe  _lprgulAccess_. Ni IPROP_READONLY ni IPROP_READWRITE sera d�finie.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-p104">If a property has been modified, its IPROP_DIRTY flag is set in the corresponding entry in the array that  _lprgulAccess_ points to. Neither IPROP_READONLY nor IPROP_READWRITE will be set.</span></span> 
  
<span data-ttu-id="a4b8f-135">Si une propri�t� n'a pas �t� modifi�e ou supprim�e, seul l'indicateur IPROP_READONLY ou IPROP_READWRITE sera d�finie.</span><span class="sxs-lookup"><span data-stu-id="a4b8f-135">If a property has not been modified or deleted, only the IPROP_READONLY or IPROP_READWRITE flag will be set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4b8f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4b8f-136">See also</span></span>



[<span data-ttu-id="a4b8f-137">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a4b8f-137">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="a4b8f-138">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a4b8f-138">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

