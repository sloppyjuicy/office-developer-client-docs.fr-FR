---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419988"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="2017f-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="2017f-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="2017f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2017f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2017f-105">Modifie définitivement une section de profil de magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="2017f-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2017f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2017f-106">Parameters</span></span>

 <span data-ttu-id="2017f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2017f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2017f-108">[in] Masque de bits d’indicateurs qui indique le type de magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="2017f-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="2017f-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="2017f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="2017f-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="2017f-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="2017f-111">La magasin de messages est temporaire et ne doit pas être ajoutée à la table de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="2017f-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="2017f-112">Lorsque MDB_TEMPORARY est définie, **ModifyProfile** S_OK immédiatement.</span><span class="sxs-lookup"><span data-stu-id="2017f-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2017f-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2017f-113">Return value</span></span>

<span data-ttu-id="2017f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="2017f-114">S_OK</span></span> 
  
> <span data-ttu-id="2017f-115">Les modifications apportées à la section de profil ont réussi.</span><span class="sxs-lookup"><span data-stu-id="2017f-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2017f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="2017f-116">Remarks</span></span>

<span data-ttu-id="2017f-117">La **méthode IMAPISupport::ModifyProfile** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="2017f-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="2017f-118">Les fournisseurs de magasins de messages **appellent ModifyProfile pour** demander à MAPI de modifier leurs informations de profil.</span><span class="sxs-lookup"><span data-stu-id="2017f-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="2017f-119">**ModifyProfile ajoute la** section de profil associée au fournisseur appelant à la liste des ressources de fournisseur de magasins de messages installées.</span><span class="sxs-lookup"><span data-stu-id="2017f-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="2017f-120">Cela entraîne la liste de la magasin de messages dans la table de la boutique de messages, accessible aux clients via la méthode [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) et ouverte sans l’affichage d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2017f-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="2017f-121">Si l’MDB_TEMPORARY est définie, MAPI ne fait rien et la méthode est immédiatement S_OK.</span><span class="sxs-lookup"><span data-stu-id="2017f-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2017f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2017f-122">See also</span></span>



[<span data-ttu-id="2017f-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="2017f-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="2017f-124">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2017f-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

