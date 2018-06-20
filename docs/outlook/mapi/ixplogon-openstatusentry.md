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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0e96c0b99f0a5f7511ed59b483ab9409eafad882
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784495"
---
# <a name="ixplogonopenstatusentry"></a><span data-ttu-id="8a6bb-103">IXPLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="8a6bb-103">IXPLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="8a6bb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a6bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a6bb-105">Ouvre l’objet d’état du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-105">Opens the transport provider's status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="8a6bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a6bb-106">Parameters</span></span>

 <span data-ttu-id="8a6bb-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8a6bb-107">_lpInterface_</span></span>
  
> <span data-ttu-id="8a6bb-108">[in] Pointeur vers un identificateur d’interface (IID) de l’objet d’ouverture de session de transport.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-108">[in] A pointer to an interface identifier (IID) for the transport logon object.</span></span> <span data-ttu-id="8a6bb-109">Passage de NULL renvoie l’interface [IMAPIStatus](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="8a6bb-109">Passing NULL returns the [IMAPIStatus](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="8a6bb-110">Le paramètre _lpInterface_ peut également avoir un identificateur pour une interface pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-110">The  _lpInterface_ parameter can also be set to an identifier for an interface for the object.</span></span> 
    
 <span data-ttu-id="8a6bb-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a6bb-111">_ulFlags_</span></span>
  
> <span data-ttu-id="8a6bb-112">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet d’état est ouvert.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="8a6bb-113">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="8a6bb-113">The following flag can be set:</span></span>
    
<span data-ttu-id="8a6bb-114">N'</span><span class="sxs-lookup"><span data-stu-id="8a6bb-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="8a6bb-115">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-115">Requests read/write permission.</span></span> <span data-ttu-id="8a6bb-116">L’interface par défaut est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-116">The default interface is read-only.</span></span> 
    
 <span data-ttu-id="8a6bb-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="8a6bb-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="8a6bb-118">[out] Pointeur vers le type de l’objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="8a6bb-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="8a6bb-119">_lppEntry_</span></span>
  
> <span data-ttu-id="8a6bb-120">[out] Pointeur vers le pointeur vers l’objet de l’état ouvert.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-120">[out] A pointer to the pointer to the opened status object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a6bb-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8a6bb-121">Return value</span></span>

<span data-ttu-id="8a6bb-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a6bb-122">S_OK</span></span> 
  
> <span data-ttu-id="8a6bb-123">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a6bb-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a6bb-124">Remarks</span></span>

<span data-ttu-id="8a6bb-125">Le spouleur MAPI appelle la méthode **IXPLogon::OpenStatusEntry** lorsqu’une application cliente appelle une méthode **OpenEntry** pour l’identificateur d’entrée dans la ligne de tableau de statut du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-125">The MAPI spooler calls the **IXPLogon::OpenStatusEntry** method when a client application calls an **OpenEntry** method for the entry identifier in the transport provider's status table row.</span></span> <span data-ttu-id="8a6bb-126">**OpenStatusEntry** ouvre un objet avec l’interface **IMAPIStatus** associé à cette connexion au fournisseur du transport particulier.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-126">**OpenStatusEntry** opens an object with the **IMAPIStatus** interface associated with this particular transport provider logon.</span></span> <span data-ttu-id="8a6bb-127">Cet objet est ensuite utilisé pour permettre aux applications clientes d’appeler des méthodes **IMAPIStatus** (par exemple, pour reconfigurer l’ouverture de session à l’aide de la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) ou pour valider l’état de l’ouverture de session à l’aide de la [ IMAPIStatus::ValidateState](imapistatus-validatestate.md) méthode).</span><span class="sxs-lookup"><span data-stu-id="8a6bb-127">This object is then used to enable client applications to call **IMAPIStatus** methods (for example, to reconfigure the logon session by using the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method, or to validate the state of the logon session by using the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8a6bb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a6bb-128">See also</span></span>



[<span data-ttu-id="8a6bb-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8a6bb-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="8a6bb-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a6bb-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

