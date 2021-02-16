---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435900"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="41011-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="41011-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="41011-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41011-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41011-105">Ouvre l’objet d’état du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="41011-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="41011-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41011-106">Parameters</span></span>

 <span data-ttu-id="41011-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="41011-107">_lpInterface_</span></span>
  
> <span data-ttu-id="41011-108">[in] Pointeur vers un identificateur d’interface (IID) pour l’objet d’identification de transport.</span><span class="sxs-lookup"><span data-stu-id="41011-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="41011-109">La transmission null renvoie [l’interface IMAPIStatus.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="41011-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="41011-110">Le  _paramètre lpInterface_ peut également être définie sur un identificateur pour une interface pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="41011-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="41011-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="41011-111">_ulFlags_</span></span>
  
> <span data-ttu-id="41011-112">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert.</span><span class="sxs-lookup"><span data-stu-id="41011-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="41011-113">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="41011-113">The following flag can be set:</span></span>
    
<span data-ttu-id="41011-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="41011-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="41011-115">Demande une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="41011-115">Requests read/write permission.</span></span> <span data-ttu-id="41011-116">L’interface par défaut est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="41011-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="41011-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="41011-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="41011-118">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="41011-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="41011-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="41011-119">_lppEntry_</span></span>
  
> <span data-ttu-id="41011-120">[out] Pointeur vers le pointeur vers l’objet d’état ouvert.</span><span class="sxs-lookup"><span data-stu-id="41011-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="41011-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41011-121">Return value</span></span>

<span data-ttu-id="41011-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="41011-122">S_OK</span></span> 
  
> <span data-ttu-id="41011-123">L’appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="41011-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41011-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="41011-124">Remarks</span></span>

<span data-ttu-id="41011-125">Lepooler MAPI appelle la méthode **IXPLogon::OpenStatusEntry** lorsqu’une application cliente appelle une méthode **OpenEntry** pour l’identificateur d’entrée dans la ligne de table d’état du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="41011-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="41011-126">**OpenStatusEntry ouvre** un objet avec l’interface **IMAPIStatus** associée à ce fournisseur de transport particulier.</span><span class="sxs-lookup"><span data-stu-id="41011-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="41011-127">Cet objet est ensuite utilisé pour permettre aux applications clientes d’appeler des méthodes **IMAPIStatus** (par exemple, pour reconfigurer la session d’ouverture de session à l’aide de la méthode [IMAPIStatus::SettingsDialog,](imapistatus-settingsdialog.md) ou pour valider l’état de la session d’ouverture de session à l’aide de la méthode [IMAPIStatus::ValidateState).](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="41011-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41011-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41011-128">See also</span></span>



[<span data-ttu-id="41011-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="41011-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="41011-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41011-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

