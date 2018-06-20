---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Ajoute la personne identifiée par le paramètre emailAddress comme un ami pour l’utilisateur connecté sur le réseau social.
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787610"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="ef34a-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="ef34a-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="ef34a-104">Ajoute la personne identifiée par le paramètre _emailAddress_ comme un ami pour l’utilisateur connecté sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="ef34a-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="ef34a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef34a-105">Parameters</span></span>

<span data-ttu-id="ef34a-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="ef34a-106">_emailAddress_</span></span>
  
> <span data-ttu-id="ef34a-107">[in] Chaîne qui contient une adresse de messagerie d’une personne.</span><span class="sxs-lookup"><span data-stu-id="ef34a-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef34a-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="ef34a-108">Remarks</span></span>

<span data-ttu-id="ef34a-109">Le paramètre _emailAddress_ doit être une adresse SMTP valide.</span><span class="sxs-lookup"><span data-stu-id="ef34a-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="ef34a-110">Si le fournisseur Outlook Social Connector (OSC) a défini la méthode **followPerson** comme **true** dans les **fonctionnalités**et l’argument pour _emailAddress_ ne correspond pas à un utilisateur sur le réseau, le fournisseur doit retourner la OSC_E_NOT_FOUND erreur.</span><span class="sxs-lookup"><span data-stu-id="ef34a-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="ef34a-111">Si le fournisseur a défini **followPerson** comme **false** de **fonctionnalités**, le fournisseur doit renvoyer l’erreur OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="ef34a-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="ef34a-112">Si le fournisseur implémente l’interface [ISocialSession2](isocialsession2iunknown.md) et a défini **followPerson** comme **true** dans les **fonctionnalités**, l’OSC appellera [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) au lieu de **ISocialSession::FollowPerson **.</span><span class="sxs-lookup"><span data-stu-id="ef34a-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="ef34a-113">Si le fournisseur n’implémente pas l’interface **ISocialSession2** ou **ISocialSession2::FollowPersonEx** renvoie l’erreur OSC_E_NOTIMPL, l’OSC appellera **ISocialSession::FollowPerson** tant que le fournisseur a la valeur ** followPerson** comme **true** dans les **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="ef34a-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="ef34a-114">Pour plus d’informations sur les codes d’erreur, voir [Codes d’erreur de fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ef34a-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="ef34a-115">Pour décider si à implémenter **ISocalSession::FollowPerson** ou **ISocialSession2::FollowPersonEx**, vous devez tenir compte si votre fournisseur doit les autres méthodes de **ISocialSession2**et si vous pouvez utiliser la _ djsplayName_ paramètre dans **FollowPersonEx**.</span><span class="sxs-lookup"><span data-stu-id="ef34a-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef34a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef34a-116">See also</span></span>

- [<span data-ttu-id="ef34a-117">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef34a-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

