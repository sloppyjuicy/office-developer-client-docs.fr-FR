---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Ajoute la personne identifiée par les paramètres emailAddresses et displayName comme un ami pour l’utilisateur connecté sur le réseau social.
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787628"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="ba2af-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="ba2af-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="ba2af-104">Ajoute la personne identifiée par les paramètres _emailAddresses_ et _displayName_ comme un ami pour l’utilisateur connecté sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="ba2af-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="ba2af-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba2af-105">Parameters</span></span>

<span data-ttu-id="ba2af-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="ba2af-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="ba2af-107">[in] Tableau qui contienne une ou plusieurs adresses SMTP valides pour une personne sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="ba2af-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="ba2af-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="ba2af-108">_displayName_</span></span>
  
> <span data-ttu-id="ba2af-109">[in] Chaîne qui contient le nom complet de la personne à ajouter comme un ami.</span><span class="sxs-lookup"><span data-stu-id="ba2af-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba2af-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba2af-110">Remarks</span></span>

<span data-ttu-id="ba2af-111">Si le Outlook Social Connector (OSC) fournit plusieurs sur adresse SMTP dans le tableau dans le paramètre **emailAddresses** , le fournisseur OSC pouvez supposer que le premier élément est l’adresse SMTP principale.</span><span class="sxs-lookup"><span data-stu-id="ba2af-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="ba2af-112">Si le fournisseur a la valeur de l’élément **followPerson** comme **true** dans le XML des **fonctionnalités** et aucun des éléments pour _emailAddresses_ correspondent à un utilisateur sur le réseau, le fournisseur doit retourner l’erreur OSC_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="ba2af-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="ba2af-113">Si le fournisseur a défini **followPerson** comme **false** de **fonctionnalités**, le fournisseur doit renvoyer l’erreur OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="ba2af-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="ba2af-114">Si la méthode **FollowPersonEx** aboutit, le fournisseur peut utiliser la chaîne dans le paramètre _displayName_ à l’adresse de la personne dans tous les messages envoyés ami-confirmation suivantes, plutôt que d’adressage de la personne à l’adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="ba2af-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="ba2af-115">En revanche, le fournisseur doit être en mesure de gérer l’OSC en passant une chaîne vide pour le paramètre _displayName_ .</span><span class="sxs-lookup"><span data-stu-id="ba2af-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="ba2af-116">Si le fournisseur implémente l’interface [ISocialSession2](isocialsession2iunknown.md) et a défini **followPerson** comme **true** dans le XML des fonctionnalités, l’OSC appelle **FollowPersonEx** au lieu de [ISocialSession::FollowPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="ba2af-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="ba2af-117">Si le fournisseur a défini **followPerson** **a la valeur True** , mais n’implémente pas l’interface **ISocialSession2** ou **FollowPersonEx** renvoie l’erreur OSC_E_NOTIMPL, l’OSC appelle **ISocialSession::FollowPerson**.</span><span class="sxs-lookup"><span data-stu-id="ba2af-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ba2af-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba2af-118">See also</span></span>

- [<span data-ttu-id="ba2af-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba2af-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

