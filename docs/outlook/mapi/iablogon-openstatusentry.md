---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410783"
---
# <a name="iablogonopenstatusentry"></a><span data-ttu-id="40dd4-103">IABLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="40dd4-103">IABLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="40dd4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40dd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40dd4-105">Ouvre l’objet d’état du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="40dd4-105">Opens the provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="40dd4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="40dd4-106">Parameters</span></span>

 <span data-ttu-id="40dd4-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="40dd4-107">_lpInterface_</span></span>
  
> <span data-ttu-id="40dd4-108">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface qui doit être utilisée pour accéder à l’objet d’état.</span><span class="sxs-lookup"><span data-stu-id="40dd4-108">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the status object.</span></span> <span data-ttu-id="40dd4-109">La transmission null renvoie l’interface standard de l’objet, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="40dd4-109">Passing NULL returns the object's standard interface, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span>
    
 <span data-ttu-id="40dd4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40dd4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="40dd4-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert.</span><span class="sxs-lookup"><span data-stu-id="40dd4-111">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="40dd4-112">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="40dd4-112">The following flag can be set:</span></span>
    
<span data-ttu-id="40dd4-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="40dd4-113">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="40dd4-114">Demande une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="40dd4-114">Requests read/write permission.</span></span> <span data-ttu-id="40dd4-115">Par défaut, les objets sont ouverts avec un accès en lecture seule et les appelants ne doivent pas supposer que l’autorisation lecture/écriture a été accordée.</span><span class="sxs-lookup"><span data-stu-id="40dd4-115">By default, objects are opened with read-only access, and callers should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="40dd4-116">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="40dd4-116">_lpulObjType_</span></span>
  
> <span data-ttu-id="40dd4-117">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="40dd4-117">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="40dd4-118">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="40dd4-118">_lppEntry_</span></span>
  
> <span data-ttu-id="40dd4-119">[out] Pointeur vers un pointeur vers l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="40dd4-119">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40dd4-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="40dd4-120">Return value</span></span>

<span data-ttu-id="40dd4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="40dd4-121">S_OK</span></span> 
  
> <span data-ttu-id="40dd4-122">L’appel a réussi et l’objet d’état a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="40dd4-122">The call succeeded and the status object has been opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40dd4-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="40dd4-123">Remarks</span></span>

<span data-ttu-id="40dd4-124">Les fournisseurs de carnets d’adresses **implémentent la méthode OpenStatusEntry** pour accorder l’accès à leur objet d’état.</span><span class="sxs-lookup"><span data-stu-id="40dd4-124">Address book providers implement the **OpenStatusEntry** method to grant access to their status object.</span></span> <span data-ttu-id="40dd4-125">Tous les fournisseurs de carnet d’adresses sont requis pour implémenter un objet d’état qui prend en charge, au minimum, la méthode [IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="40dd4-125">All address book providers are required to implement a status object that supports, at a minimum, the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="40dd4-126">Pour plus d’informations, voir [Status Object Implementation](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="40dd4-126">For more information, see [Status Object Implementation](status-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40dd4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40dd4-127">See also</span></span>



[<span data-ttu-id="40dd4-128">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="40dd4-128">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="40dd4-129">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="40dd4-129">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="40dd4-130">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="40dd4-130">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="40dd4-131">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40dd4-131">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

