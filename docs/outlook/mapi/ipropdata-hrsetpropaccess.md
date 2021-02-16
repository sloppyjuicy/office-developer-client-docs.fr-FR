---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9e443302e49bad4a586b657a6de298dafbeefab4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437853"
---
# <a name="ipropdatahrsetpropaccess"></a><span data-ttu-id="c9dea-103">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="c9dea-103">IPropData::HrSetPropAccess</span></span>

  
  
<span data-ttu-id="c9dea-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9dea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9dea-105">D�finit le niveau d'acc�s ou un �tat pour un ou plusieurs des propri�t�s de l'objet.</span><span class="sxs-lookup"><span data-stu-id="c9dea-105">Sets the access level or status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="c9dea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9dea-106">Parameters</span></span>

 <span data-ttu-id="c9dea-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="c9dea-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c9dea-108">[in] Pointeur vers un tableau de balises de propri�t�s qui indiquent les propri�t�s � modifier.</span><span class="sxs-lookup"><span data-stu-id="c9dea-108">[in] A pointer to an array of property tags that indicate the properties to be modified.</span></span> 
    
 <span data-ttu-id="c9dea-109">_rgulAccess_</span><span class="sxs-lookup"><span data-stu-id="c9dea-109">_rgulAccess_</span></span>
  
> <span data-ttu-id="c9dea-p101">[in] Tableau des masques de bits indicateur. Chaque masque de bits indique les niveaux d'acc�s ou �tat ou les deux, pour chacune des propri�t�s identifi�es dans le tableau vers laquelle pointe le param�tre  _lpPropTagArray_. Les deux tableaux sont positionnels dans la mesure o� le premier masque de bits dans  _rgulAccess_ d�crit la premi�re propri�t� qui pointe  _lpPropTagArray_, et ainsi de suite. Pour chaque balise de propri�t�, un indicateur de niveau d'acc�s et l'indicateur d'�tat d'un seul peut �tre d�finie. Le tableau suivant pr�sente les indicateurs possibles.</span><span class="sxs-lookup"><span data-stu-id="c9dea-p101">[in] An array of flag bitmasks. Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array that the  _lpPropTagArray_ parameter points to. The two arrays are positional in that the first bitmask in  _rgulAccess_ describes the first property that  _lpPropTagArray_ points to, and so on. For each property tag, one access-level flag and one status flag can be set. The following table shows the possible flags.</span></span> 
    
|<span data-ttu-id="c9dea-115">**Indicateur de niveau d'acc�s**</span><span class="sxs-lookup"><span data-stu-id="c9dea-115">**Access-level flag**</span></span>|<span data-ttu-id="c9dea-116">**Indicateur d'�tat**</span><span class="sxs-lookup"><span data-stu-id="c9dea-116">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9dea-117">IPROP_READONLY, ce qui indique que la propri�t� ne peut pas �tre modifi�e.</span><span class="sxs-lookup"><span data-stu-id="c9dea-117">IPROP_READONLY, which indicates that the property cannot be modified</span></span>  <br/> |<span data-ttu-id="c9dea-118">IPROP_CLEAN, ce qui indique que la propri�t� n'a pas �t� modifi�e.</span><span class="sxs-lookup"><span data-stu-id="c9dea-118">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="c9dea-119">IPROP_READWRITE, ce qui indique que la propri�t� peut �tre modifi�e.</span><span class="sxs-lookup"><span data-stu-id="c9dea-119">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="c9dea-120">IPROP_DIRTY, ce qui indique que la propri�t� a �t� modifi�e.</span><span class="sxs-lookup"><span data-stu-id="c9dea-120">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="c9dea-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c9dea-121">Return value</span></span>

<span data-ttu-id="c9dea-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9dea-122">S_OK</span></span> 
  
> <span data-ttu-id="c9dea-123">Les indicateurs d'�tat et le niveau d'acc�s ont �t� correctement d�finis.</span><span class="sxs-lookup"><span data-stu-id="c9dea-123">The access-level and status flags have been successfully set.</span></span>
    
<span data-ttu-id="c9dea-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c9dea-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c9dea-125">Une tentative a �t� effectu�e pour d�finir la propri�t� sur un objet en lecture seule ou d'un objet pour lequel l'appelant dispose d'autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="c9dea-125">An attempt was made to set a property on a read-only object or an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="c9dea-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c9dea-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c9dea-127">Le param�tre  _rgulAccess_ contient une combinaison d'indicateurs, tels que IPROP_READONLY et IPROP_READWRITE non valide.</span><span class="sxs-lookup"><span data-stu-id="c9dea-127">The  _rgulAccess_ parameter contains an invalid combination of flags, such as IPROP_READONLY and IPROP_READWRITE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c9dea-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9dea-128">Remarks</span></span>

<span data-ttu-id="c9dea-p102">La m�thode **IPropData::HrSetPropAccess** modifie le niveau d'acc�s et l'�tat pour les propri�t�s qui sont identifi�es par les balises de propri�t� dans la structure [SPropTagArray](sproptagarray.md) d�sign�s par le param�tre  _lpPropTagArray_. Pour chaque propri�t�, il existe une entr�e correspondante dans le tableau  _rgulAccess_. L'entr�e peut �tre d�finie sur un indicateur qui indique le niveau d'acc�s de la propri�t� et l'autre indicateur indiquant son statut.</span><span class="sxs-lookup"><span data-stu-id="c9dea-p102">The **IPropData::HrSetPropAccess** method changes the access level and status for the properties that are identified by the property tags in the [SPropTagArray](sproptagarray.md) structure pointed to by the  _lpPropTagArray_ parameter. For each property, there is a corresponding entry in the  _rgulAccess_ array. The entry can be set to one flag that indicates the property's access level and another flag that indicates its status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9dea-132">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="c9dea-132">Notes to callers</span></span>

<span data-ttu-id="c9dea-133">Utilisez **HrSetPropAccess** pour d�terminer quand une valeur de propri�t� particuli�re change et modifier le niveau d'acc�s pour un ou plusieurs des propri�t�s d'un objet.</span><span class="sxs-lookup"><span data-stu-id="c9dea-133">Use **HrSetPropAccess** to determine when a particular property value changes and to change the access level for one or more of an object's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9dea-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9dea-134">See also</span></span>



[<span data-ttu-id="c9dea-135">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c9dea-135">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="c9dea-136">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c9dea-136">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

