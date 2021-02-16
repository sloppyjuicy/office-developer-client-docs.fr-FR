---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Supprime la personne identifiée par le paramètre userID en tant qu’ami sur le réseau social.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418434"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="1f93f-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="1f93f-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="1f93f-104">Supprime la personne identifiée par le paramètre  _userID_ en tant qu’ami sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="1f93f-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="1f93f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f93f-105">Parameters</span></span>

<span data-ttu-id="1f93f-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="1f93f-106">_userID_</span></span>
  
> <span data-ttu-id="1f93f-107">[in] Chaîne qui contient un ID d’utilisateur de réseau social pour une personne.</span><span class="sxs-lookup"><span data-stu-id="1f93f-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f93f-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="1f93f-108">Remarks</span></span>

<span data-ttu-id="1f93f-109">Le  _paramètre userID_ doit être un ID d’utilisateur valide pour la personne sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="1f93f-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="1f93f-110">Si le fournisseur Outlook Social Connector (OSC) a définie **doNotFollowPerson** comme **true** dans le XML pour les fonctionnalités, le fournisseur doit renvoyer l’erreur OSC_E_NOT_FOUND dans le cas où l’ID d’utilisateur transmis ne correspond pas à un utilisateur sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="1f93f-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="1f93f-111">Si le fournisseur a définie **doNotFollowPerson** comme **false** dans les **fonctionnalités,** le fournisseur doit renvoyer l’OSC_E_FAIL erreur.</span><span class="sxs-lookup"><span data-stu-id="1f93f-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="1f93f-112">Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1f93f-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1f93f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f93f-113">See also</span></span>

- [<span data-ttu-id="1f93f-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f93f-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

