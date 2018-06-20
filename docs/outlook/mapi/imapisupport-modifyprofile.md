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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 98e6331d5a9e52d5ae73ed12d8c045bdf226c2c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783996"
---
# <a name="imapisupportmodifyprofile"></a><span data-ttu-id="ae2f5-103">IMAPISupport::ModifyProfile</span><span class="sxs-lookup"><span data-stu-id="ae2f5-103">IMAPISupport::ModifyProfile</span></span>

  
  
<span data-ttu-id="ae2f5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae2f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae2f5-105">Modifie un message stocker la section profil définitive.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-105">Makes changes to a message store profile section permanent.</span></span>
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ae2f5-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="ae2f5-106">Parameters</span></span>

 <span data-ttu-id="ae2f5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ae2f5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ae2f5-108">[in] Magasin de masque de bits d’indicateurs qui indique le type de message.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-108">[in] A bitmask of flags that indicates the type of message store.</span></span> <span data-ttu-id="ae2f5-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="ae2f5-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ae2f5-110">MDB_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="ae2f5-110">MDB_TEMPORARY</span></span> 
  
> <span data-ttu-id="ae2f5-111">La banque de messages est temporaire et ne doit pas être ajoutée à la table.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-111">The message store is temporary and should not be added to the message store table.</span></span> <span data-ttu-id="ae2f5-112">Lorsque la valeur MDB_TEMPORARY, **ModifyProfile** renvoie S_OK immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-112">When MDB_TEMPORARY is set, **ModifyProfile** returns S_OK immediately.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ae2f5-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ae2f5-113">Return value</span></span>

<span data-ttu-id="ae2f5-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae2f5-114">S_OK</span></span> 
  
> <span data-ttu-id="ae2f5-115">Les modifications apportées à la section profil ont réussi.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-115">The changes to the profile section were successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae2f5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ae2f5-116">Remarks</span></span>

<span data-ttu-id="ae2f5-117">La méthode **IMAPISupport::ModifyProfile** est implémentée pour les objets de prise en charge de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-117">The **IMAPISupport::ModifyProfile** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="ae2f5-118">Magasin de fournisseurs appel **ModifyProfile** pour demander MAPI pour modifier leurs informations de profil du message.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-118">Message store providers call **ModifyProfile** to prompt MAPI to modify their profile information.</span></span> 
  
 <span data-ttu-id="ae2f5-119">**ModifyProfile** ajoute la section profil qui est associée avec le fournisseur d’appel à la liste des ressources de fournisseur de magasin de message installé.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-119">**ModifyProfile** adds the profile section that is associated with the calling provider to the list of installed message store provider resources.</span></span> <span data-ttu-id="ae2f5-120">Cela entraîne la banque de messages pour être répertoriée dans le tableau de magasin de message, qui est disponible pour les clients par le biais de la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) et s’ouvre sans l’affichage d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-120">This causes the message store to be listed in the message store table, which is available to clients through the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method, and to be opened without the display of a dialog box.</span></span> 
  
<span data-ttu-id="ae2f5-121">Si l’indicateur MDB_TEMPORARY est défini, MAPI n’a aucun effet et la méthode retourne immédiatement à S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae2f5-121">If the MDB_TEMPORARY flag is set, MAPI does nothing and the method returns immediately with S_OK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae2f5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae2f5-122">See also</span></span>



[<span data-ttu-id="ae2f5-123">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="ae2f5-123">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="ae2f5-124">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae2f5-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

