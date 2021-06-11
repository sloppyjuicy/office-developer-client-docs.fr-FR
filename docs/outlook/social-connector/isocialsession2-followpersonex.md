---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Ajoute la personne identifiée par les paramètres emailAddresses et displayName en tant qu’ami de l’utilisateur connecté sur le réseau social.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429830"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="8d248-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="8d248-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="8d248-104">Ajoute la personne identifiée par les paramètres  _emailAddresses_ et  _displayName_ en tant qu’ami de l’utilisateur connecté sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="8d248-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="8d248-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="8d248-105">Parameters</span></span>

<span data-ttu-id="8d248-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="8d248-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="8d248-107">[in] Tableau qui contient une ou plusieurs adresses SMTP valides pour une personne sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="8d248-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="8d248-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="8d248-108">_displayName_</span></span>
  
> <span data-ttu-id="8d248-109">[in] Chaîne qui contient le nom complet de la personne à ajouter en tant qu’ami.</span><span class="sxs-lookup"><span data-stu-id="8d248-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d248-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d248-110">Remarks</span></span>

<span data-ttu-id="8d248-111">Si Outlook Social Connector (OSC) fournit davantage que l’adresse SMTP dans le tableau dans le paramètre **emailAddresses,** le fournisseur OSC peut supposer que le premier élément est l’adresse SMTP principale.</span><span class="sxs-lookup"><span data-stu-id="8d248-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="8d248-112">Si le fournisseur a définie l’élément **followPerson** comme **vrai** dans le **XML** de fonctionnalités et qu’aucun des éléments pour  _emailAddresses_ ne correspond à un utilisateur sur le réseau, le fournisseur doit renvoyer l’erreur OSC_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="8d248-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="8d248-113">Si le fournisseur a définie **followPerson** comme **false** dans les **fonctionnalités,** le fournisseur doit renvoyer l’OSC_E_FAIL erreur.</span><span class="sxs-lookup"><span data-stu-id="8d248-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="8d248-114">Si la méthode **FollowPersonEx** réussit, le fournisseur peut utiliser la chaîne dans le paramètre  _displayName_ pour adresser la personne dans n’importe quel e-mail de confirmation d’ami ultérieur, plutôt que d’adresser la personne par l’adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="8d248-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="8d248-115">En revanche, le fournisseur doit être en mesure de gérer l’OSC en passant une chaîne vide pour le _paramètre displayName._</span><span class="sxs-lookup"><span data-stu-id="8d248-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="8d248-116">Si le fournisseur implémente l’interface [ISocialSession2](isocialsession2iunknown.md) et a définie **followPerson** comme **true** dans les fonctionnalités XML, l’OSC appelle **FollowPersonEx** au lieu de [ISocialSession::FollowPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="8d248-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="8d248-117">Si le fournisseur a définie **followPerson** comme **true** mais n’implémente pas l’interface **ISocialSession2,** ou **si FollowPersonEx** renvoie l’erreur OSC_E_NOTIMPL, l’OSC appelle **ISocialSession::FollowPerson**.</span><span class="sxs-lookup"><span data-stu-id="8d248-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d248-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d248-118">See also</span></span>

- [<span data-ttu-id="8d248-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d248-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

