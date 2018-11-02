---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a48d8248878c64de827bb09030073e6becba3024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571198"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="cc1b2-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="cc1b2-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="cc1b2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc1b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc1b2-105">Ouvre un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="cc1b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc1b2-106">Parameters</span></span>

 <span data-ttu-id="cc1b2-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="cc1b2-107">_lpInterface_</span></span>
  
> <span data-ttu-id="cc1b2-108">[in] Pointeur vers l’identificateur d’interface (IID) pour l’objet d’état à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="cc1b2-109">Valeur null indique l’interface standard pour l’objet est retournée (dans ce cas, l’interface [IMAPIStatus](imapistatusimapiprop.md) ).</span><span class="sxs-lookup"><span data-stu-id="cc1b2-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="cc1b2-110">Le paramètre _lpInterface_ peut également être défini à un identificateur pour une interface appropriée pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="cc1b2-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cc1b2-111">_ulFlags_</span></span>
  
> <span data-ttu-id="cc1b2-112">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="cc1b2-113">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="cc1b2-113">The following flag can be set:</span></span>
    
<span data-ttu-id="cc1b2-114">N'</span><span class="sxs-lookup"><span data-stu-id="cc1b2-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="cc1b2-115">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-115">Requests read/write permission.</span></span> <span data-ttu-id="cc1b2-116">Par défaut, les objets sont créés avec l’autorisation en lecture seule, et les applications clientes ne doivent pas fonctionner sur l’hypothèse que bénéficie des autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="cc1b2-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="cc1b2-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="cc1b2-118">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="cc1b2-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="cc1b2-119">_lppEntry_</span></span>
  
> <span data-ttu-id="cc1b2-120">[out] Pointeur vers le pointeur vers l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc1b2-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc1b2-121">Return value</span></span>

<span data-ttu-id="cc1b2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc1b2-122">S_OK</span></span> 
  
> <span data-ttu-id="cc1b2-123">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cc1b2-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="cc1b2-124">Remarks</span></span>

<span data-ttu-id="cc1b2-125">Fournisseurs de magasins message implémentent la méthode **IMSLogon::OpenStatusEntry** pour ouvrir un objet d’état.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="cc1b2-126">Cet objet état sert ensuite pour permettre aux clients d’appeler des méthodes [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="cc1b2-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="cc1b2-127">Par exemple, les clients peuvent utiliser la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour reconfigurer la session d’ouverture de session du magasin de message ou la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) pour valider l’état de la session d’ouverture de session du magasin de message.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc1b2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc1b2-128">See also</span></span>



[<span data-ttu-id="cc1b2-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cc1b2-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="cc1b2-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="cc1b2-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="cc1b2-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cc1b2-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="cc1b2-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc1b2-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

