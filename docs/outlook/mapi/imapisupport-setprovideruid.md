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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326312"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="d8ae0-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="d8ae0-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="d8ae0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8ae0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8ae0-105">Inscrit une structure [MAPIUID](mapiuid.md) qui représente le fournisseur de services de manière unique.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d8ae0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8ae0-106">Parameters</span></span>

 <span data-ttu-id="d8ae0-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="d8ae0-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="d8ae0-108">dans Pointeur vers la structure **MAPIUID** qui identifie le carnet d'adresses ou le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="d8ae0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8ae0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d8ae0-110">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8ae0-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d8ae0-111">Return value</span></span>

<span data-ttu-id="d8ae0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8ae0-112">S_OK</span></span> 
  
> <span data-ttu-id="d8ae0-113">La structure **MAPIUID** a été correctement inscrite.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d8ae0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d8ae0-114">Remarks</span></span>

<span data-ttu-id="d8ae0-115">La méthode **IMAPISupport:: SetProviderUID** est implémentée pour les objets de prise en charge du carnet d'adresses et du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="d8ae0-116">Ces fournisseurs appellent **SetProviderUID** pour enregistrer un identificateur unique décrit dans la structure **MAPIUID** pointée par _lpProviderID_.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="d8ae0-117">Les fournisseurs incluent cet identificateur dans tous les identificateurs d'entrée qu'ils créent.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="d8ae0-118">MAPI utilise la structure **MAPIUID** lorsqu'il envoie des messages sortants vers le spouleur MAPI et détermine le fournisseur approprié pour la gestion des demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="d8ae0-119">Par exemple, lorsqu'un client appelle la méthode [IMAPISession:: OpenEntry](imapisession-openentry.md) , MAPI examine la partie **MAPIUID** de l'identificateur d'entrée, la mappe au fournisseur qui l'a passée à **SetProviderUID**et appelle le **OpenEntry** de ce fournisseur. .</span><span class="sxs-lookup"><span data-stu-id="d8ae0-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d8ae0-120">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="d8ae0-120">Notes to callers</span></span>

<span data-ttu-id="d8ae0-121">Appelez **SetProviderUID** au moment de l'ouverture de session pour enregistrer votre structure **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="d8ae0-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="d8ae0-122">MAPI permet aux fournisseurs de carnets d'adresses et de banques de messages d'enregistrer plusieurs identificateurs.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="d8ae0-123">Lorsque vous effectuez plusieurs appels à **SetProviderUID**, il ajoute toujours la structure **MAPIUID** au jeu de structures **MAPIUID** du fournisseur, même si le **MAPIUID** est un doublon.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="d8ae0-124">**SetProviderUID** ne peut pas supprimer un **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8ae0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8ae0-125">See also</span></span>



[<span data-ttu-id="d8ae0-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d8ae0-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d8ae0-127">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8ae0-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

