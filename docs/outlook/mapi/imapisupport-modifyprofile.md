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
ms.openlocfilehash: b16730681b5414f28ae45be7195b4fa551bf0e82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591988"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="33f26-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="33f26-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="33f26-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33f26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33f26-105">Modifie un message stocker la section profil définitive.</span><span class="sxs-lookup"><span data-stu-id="33f26-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="33f26-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="33f26-106">Parameters</span></span>

 <span data-ttu-id="33f26-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="33f26-107">_ulFlags_</span></span>
  
> <span data-ttu-id="33f26-108">[in] Magasin de masque de bits d’indicateurs qui indique le type de message.</span><span class="sxs-lookup"><span data-stu-id="33f26-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="33f26-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="33f26-109">The following flag can be set:</span></span>
    
<span data-ttu-id="33f26-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="33f26-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="33f26-111">La banque de messages est temporaire et ne doit pas être ajoutée à la table.</span><span class="sxs-lookup"><span data-stu-id="33f26-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="33f26-112">Lorsque la valeur MDB_TEMPORARY, **ModifyProfile** renvoie S_OK immédiatement.</span><span class="sxs-lookup"><span data-stu-id="33f26-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="33f26-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="33f26-113">Return value</span></span>

<span data-ttu-id="33f26-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="33f26-114">S_OK</span></span> 
  
> <span data-ttu-id="33f26-115">Les modifications apportées à la section profil ont réussi.</span><span class="sxs-lookup"><span data-stu-id="33f26-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33f26-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="33f26-116">Remarks</span></span>

<span data-ttu-id="33f26-117">La méthode **IMAPISupport::ModifyProfile** est implémentée pour les objets de prise en charge de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="33f26-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="33f26-118">Magasin de fournisseurs appel **ModifyProfile** pour demander MAPI pour modifier leurs informations de profil du message.</span><span class="sxs-lookup"><span data-stu-id="33f26-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="33f26-119">**ModifyProfile** ajoute la section profil qui est associée avec le fournisseur d’appel à la liste des ressources de fournisseur de magasin de message installé.</span><span class="sxs-lookup"><span data-stu-id="33f26-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="33f26-120">Cela entraîne la banque de messages pour être répertoriée dans le tableau de magasin de message, qui est disponible pour les clients par le biais de la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) et s’ouvre sans l’affichage d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="33f26-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="33f26-121">Si l’indicateur MDB_TEMPORARY est défini, MAPI n’a aucun effet et la méthode retourne immédiatement à S_OK.</span><span class="sxs-lookup"><span data-stu-id="33f26-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33f26-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33f26-122">See also</span></span>



[<span data-ttu-id="33f26-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="33f26-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="33f26-124">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33f26-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

