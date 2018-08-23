---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: df842e633f1586d6d77441126d51b2ce44ec3beb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589069"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="b707f-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="b707f-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="b707f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b707f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b707f-105">Enregistre une structure [MAPIUID](mapiuid.md) qui représente le fournisseur de services de manière unique.</span><span class="sxs-lookup"><span data-stu-id="b707f-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b707f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b707f-106">Parameters</span></span>

 <span data-ttu-id="b707f-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="b707f-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="b707f-108">[in] Pointeur vers la structure **MAPIUID** qui identifie le fournisseur de banque de message ou de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b707f-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="b707f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b707f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b707f-110">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b707f-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b707f-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b707f-111">Return value</span></span>

<span data-ttu-id="b707f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b707f-112">S_OK</span></span> 
  
> <span data-ttu-id="b707f-113">La structure **MAPIUID** a été enregistrée avec succès.</span><span class="sxs-lookup"><span data-stu-id="b707f-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b707f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b707f-114">Remarks</span></span>

<span data-ttu-id="b707f-115">La méthode **IMAPISupport::SetProviderUID** est implémentée pour adresse livre et message fournisseur prise en charge des objets store.</span><span class="sxs-lookup"><span data-stu-id="b707f-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="b707f-116">Ces fournisseurs appellent **SetProviderUID** pour inscrire un identificateur unique décrit dans la structure **MAPIUID** qui est indiquée par _lpProviderID_.</span><span class="sxs-lookup"><span data-stu-id="b707f-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="b707f-117">Fournisseurs d’incluent cet identificateur dans tous les identificateurs d’entrée qu’ils créent.</span><span class="sxs-lookup"><span data-stu-id="b707f-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="b707f-118">MAPI utilise la structure **MAPIUID** lorsqu’il envoie les messages sortants pour le spouleur MAPI et pour déterminer le fournisseur approprié pour la gestion des demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="b707f-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="b707f-119">Par exemple, lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) , examine la partie **MAPIUID** de l’identificateur d’entrée MAPI, est mappé au fournisseur qui transmis aux **SetProviderUID**et appelle de ce fournisseur **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="b707f-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b707f-120">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="b707f-120">Notes to callers</span></span>

<span data-ttu-id="b707f-121">Appelez **SetProviderUID** au moment de l’ouverture de session pour inscrire votre structure **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="b707f-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="b707f-122">MAPI permet adresse livre et message fournisseurs de magasins inscrire plusieurs identificateurs.</span><span class="sxs-lookup"><span data-stu-id="b707f-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="b707f-123">Lorsque vous effectuez plusieurs appels vers **SetProviderUID**, ajoute toujours la structure **MAPIUID** pour l’ensemble du fournisseur de structures **MAPIUID** , même si le **MAPIUID** est un doublon.</span><span class="sxs-lookup"><span data-stu-id="b707f-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="b707f-124">Impossible de supprimer un **MAPIUID** **SetProviderUID** .</span><span class="sxs-lookup"><span data-stu-id="b707f-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b707f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b707f-125">See also</span></span>



[<span data-ttu-id="b707f-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b707f-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="b707f-127">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b707f-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

