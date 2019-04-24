---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330197"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="48e38-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="48e38-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="48e38-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48e38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48e38-105">Crée une nouvelle structure [MAPIUID](mapiuid.md) à utiliser comme identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="48e38-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="48e38-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48e38-106">Parameters</span></span>

 <span data-ttu-id="48e38-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="48e38-107">_lpMuid_</span></span>
  
> <span data-ttu-id="48e38-108">Pointeur vers la nouvelle structure **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="48e38-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48e38-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="48e38-109">Return value</span></span>

<span data-ttu-id="48e38-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="48e38-110">S_OK</span></span> 
  
> <span data-ttu-id="48e38-111">La nouvelle structure **MAPIUID** a été créée.</span><span class="sxs-lookup"><span data-stu-id="48e38-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="48e38-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="48e38-112">Remarks</span></span>

<span data-ttu-id="48e38-113">La méthode **IMAPISupport:: NewUID** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="48e38-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="48e38-114">Les fournisseurs de services et les services de messagerie appellent **NewUID** chaque fois qu'ils ont besoin de générer un identificateur unique à long terme.</span><span class="sxs-lookup"><span data-stu-id="48e38-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="48e38-115">Un fournisseur de banque de messages, par exemple, peut appeler **NewUID** pour obtenir un **MAPIUID** à placer dans la propriété **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) d'un message nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="48e38-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="48e38-116">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="48e38-116">Notes to callers</span></span>

<span data-ttu-id="48e38-117">Ne confondez pas la structure **MAPIUID** que vous enregistrez à l'ouverture de session avec les structures **MAPIUID** créées par la méthode **NewUID** .</span><span class="sxs-lookup"><span data-stu-id="48e38-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="48e38-118">La structure **MAPIUID** que vous enregistrez lorsque vous appelez la méthode [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) représente votre carnet d'adresses ou votre fournisseur de banque de messages dans MAPI et est utilisé pour distinguer les identificateurs d'entrée créés par différents fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="48e38-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="48e38-119">Cette structure **MAPIUID** doit être codée en dur et non obtenue via un appel à **NewUID**.</span><span class="sxs-lookup"><span data-stu-id="48e38-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="48e38-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48e38-120">See also</span></span>



[<span data-ttu-id="48e38-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="48e38-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="48e38-122">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48e38-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

