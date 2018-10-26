---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 761228a01e0dc778b962c62436e872ff20d72088
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586311"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="c0410-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="c0410-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="c0410-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0410-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0410-105">Lance le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="c0410-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c0410-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="c0410-106">Parameters</span></span>

 <span data-ttu-id="c0410-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0410-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c0410-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="c0410-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0410-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c0410-109">Return value</span></span>

<span data-ttu-id="c0410-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0410-110">S_OK</span></span> 
  
> <span data-ttu-id="c0410-111">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c0410-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="c0410-112">Si rien d’autre que S_OK est retourné, le fournisseur est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="c0410-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0410-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0410-113">Remarks</span></span>

<span data-ttu-id="c0410-114">Le spouleur MAPI appelle la méthode **IXPLogon::TransportLogoff** pour mettre fin à une session de fournisseur de transport pour un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="c0410-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="c0410-115">Avant d’appeler **TransportLogoff**, le spouleur MAPI ignore les données sur les types d’adresse de messagerie pris en charge pour cette session passée dans la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="c0410-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c0410-116">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="c0410-116">Notes to implementers</span></span>

<span data-ttu-id="c0410-117">Le fournisseur de transport doit être préparé pour accepter un appel à **TransportLogoff** à tout moment.</span><span class="sxs-lookup"><span data-stu-id="c0410-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="c0410-118">Si un message est en cours, le fournisseur doit arrêter le processus d’envoi.</span><span class="sxs-lookup"><span data-stu-id="c0410-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="c0410-119">Le fournisseur de transport doit libérer toutes les ressources alloués pour la session en cours.</span><span class="sxs-lookup"><span data-stu-id="c0410-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="c0410-120">Si elle a alloué de la mémoire pour cette session avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , il doit libérer de la mémoire à l’aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c0410-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="c0410-121">Mémoire allouée par le fournisseur de transport pour répondre aux appels à la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) peut être annulée en toute sécurité à ce stade.</span><span class="sxs-lookup"><span data-stu-id="c0410-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="c0410-122">En règle générale, sur la réalisation d’un appel **TransportLogoff** , un fournisseur doit tout d’abord invalider son objet d’ouverture de session en appelant la méthode [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) , puis son objet prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c0410-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="c0410-123">L’implémentation du fournisseur de **TransportLogoff** doit libérer l’objet de prise en charge, car lorsque l’objet de prise en charge est lancé, le spouleur MAPI peut également libérer l’objet fournisseur lui-même.</span><span class="sxs-lookup"><span data-stu-id="c0410-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0410-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0410-124">See also</span></span>



[<span data-ttu-id="c0410-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="c0410-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="c0410-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="c0410-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="c0410-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="c0410-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="c0410-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c0410-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c0410-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c0410-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c0410-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0410-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

