---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Supprime la personne identifiée par le paramètre userID comme un ami sur le réseaux sociaux.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787619"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="e5af7-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="e5af7-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="e5af7-104">Supprime la personne identifiée par le paramètre _userID_ comme un ami sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="e5af7-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="e5af7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5af7-105">Parameters</span></span>

<span data-ttu-id="e5af7-106">_nom d’utilisateur_</span><span class="sxs-lookup"><span data-stu-id="e5af7-106">_userID_</span></span>
  
> <span data-ttu-id="e5af7-107">[in] Chaîne qui contient un ID d’utilisateur de réseau social d’une personne.</span><span class="sxs-lookup"><span data-stu-id="e5af7-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5af7-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="e5af7-108">Remarks</span></span>

<span data-ttu-id="e5af7-109">Le paramètre _userID_ doit être un ID d’utilisateur valide pour la personne sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="e5af7-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="e5af7-110">Si le fournisseur Outlook Social Connector (OSC) a configuré **doNotFollowPerson** comme **true** dans le code XML des **capacités**, le fournisseur doit retourner l’erreur OSC_E_NOT_FOUND dans ce cas que l’utilisateur QU'ID transmis ne correspond pas à un utilisateur sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="e5af7-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="e5af7-111">Si le fournisseur a défini **doNotFollowPerson** comme **false** de **fonctionnalités**, le fournisseur doit renvoyer l’erreur OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="e5af7-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="e5af7-112">Pour plus d’informations sur les codes d’erreur, voir [Codes d’erreur de fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e5af7-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e5af7-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5af7-113">See also</span></span>

- [<span data-ttu-id="e5af7-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5af7-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

