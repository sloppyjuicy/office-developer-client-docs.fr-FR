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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351582"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="53aba-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="53aba-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="53aba-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53aba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53aba-105">Lance le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="53aba-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="53aba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53aba-106">Parameters</span></span>

 <span data-ttu-id="53aba-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53aba-107">_ulFlags_</span></span>
  
> <span data-ttu-id="53aba-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="53aba-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53aba-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53aba-109">Return value</span></span>

<span data-ttu-id="53aba-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="53aba-110">S_OK</span></span> 
  
> <span data-ttu-id="53aba-111">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="53aba-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="53aba-112">Si un élément autre que S_OK est renvoyé, le fournisseur est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="53aba-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53aba-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="53aba-113">Remarks</span></span>

<span data-ttu-id="53aba-114">Le spouleur MAPI appelle la méthode **IXPLogon:: TransportLogoff** pour mettre fin à une session de fournisseur de transport pour un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="53aba-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="53aba-115">Avant d'appeler **TransportLogoff**, le spouleur MAPI ignore les données relatives aux types d'adresses de messagerie pris en charge pour cette session passée dans la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="53aba-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="53aba-116">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="53aba-116">Notes to implementers</span></span>

<span data-ttu-id="53aba-117">Le fournisseur de transport doit être prêt à accepter un appel à **TransportLogoff** à tout moment.</span><span class="sxs-lookup"><span data-stu-id="53aba-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="53aba-118">Si un message est en cours d'opération, le fournisseur doit arrêter le processus d'envoi.</span><span class="sxs-lookup"><span data-stu-id="53aba-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="53aba-119">Le fournisseur de transport doit libérer toutes les ressources allouées pour sa session actuelle.</span><span class="sxs-lookup"><span data-stu-id="53aba-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="53aba-120">Si elle a alloué de la mémoire pour cette session à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , elle doit libérer la mémoire à l'aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="53aba-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="53aba-121">Toute mémoire allouée par le fournisseur de transport pour satisfaire les appels à la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) peut être publiée en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="53aba-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="53aba-122">En règle générale, lors de l'exécution d'un appel **TransportLogoff** , un fournisseur doit d'abord invalider son objet Logon en appelant la méthode [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) , puis libérer son objet support.</span><span class="sxs-lookup"><span data-stu-id="53aba-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="53aba-123">L'implémentation du fournisseur de **TransportLogoff** doit libérer le dernier objet de prise en charge, car lorsque l'objet de support est publié, le spouleur MAPI peut également libérer l'objet fournisseur lui-même.</span><span class="sxs-lookup"><span data-stu-id="53aba-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53aba-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53aba-124">See also</span></span>



[<span data-ttu-id="53aba-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="53aba-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="53aba-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="53aba-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="53aba-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="53aba-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="53aba-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="53aba-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="53aba-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="53aba-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="53aba-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53aba-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

