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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 244087c41e33e470c42434e9d57cee7317bcb78c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571688"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="cbb98-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="cbb98-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="cbb98-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbb98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbb98-105">Crée une nouvelle structure [MAPIUID](mapiuid.md) pour être utilisé comme un identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="cbb98-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="cbb98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbb98-106">Parameters</span></span>

 <span data-ttu-id="cbb98-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="cbb98-107">_lpMuid_</span></span>
  
> <span data-ttu-id="cbb98-108">Pointeur vers la nouvelle structure **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="cbb98-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cbb98-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="cbb98-109">Return value</span></span>

<span data-ttu-id="cbb98-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbb98-110">S_OK</span></span> 
  
> <span data-ttu-id="cbb98-111">La nouvelle structure **MAPIUID** a été créée.</span><span class="sxs-lookup"><span data-stu-id="cbb98-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cbb98-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="cbb98-112">Remarks</span></span>

<span data-ttu-id="cbb98-113">La méthode **IMAPISupport::NewUID** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cbb98-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="cbb98-114">Fournisseurs de services et les services de messagerie appellent **NewUID** chaque fois qu’ils ont besoin de générer un identificateur unique à long terme.</span><span class="sxs-lookup"><span data-stu-id="cbb98-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="cbb98-115">Un message banque fournisseur, par exemple, peut appeler **NewUID** pour obtenir un **MAPIUID** dans la propriété **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) d’un message nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="cbb98-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="cbb98-116">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="cbb98-116">Notes to callers</span></span>

<span data-ttu-id="cbb98-117">Ne confondez pas la structure **MAPIUID** que vous inscrivez au moment de l’ouverture de session avec la méthode **NewUID** crée les structures de **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="cbb98-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="cbb98-118">La structure **MAPIUID** que vous enregistrez lorsque vous appelez la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) représente votre carnet d’adresses ou message stocker fournisseur MAPI et est utilisé pour distinguer les identificateurs d’entrée qui créent des fournisseurs différents.</span><span class="sxs-lookup"><span data-stu-id="cbb98-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="cbb98-119">Cette structure **MAPIUID** doit être codées en dur et pas obtenue par un appel à **NewUID**.</span><span class="sxs-lookup"><span data-stu-id="cbb98-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cbb98-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbb98-120">See also</span></span>



[<span data-ttu-id="cbb98-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cbb98-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cbb98-122">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb98-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

