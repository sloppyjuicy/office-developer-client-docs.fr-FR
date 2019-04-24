---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Ajoute la personne identifiée par les paramètres emailAddresses et displayName comme un ami pour l'utilisateur connecté sur le réseau social.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339654"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="14390-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="14390-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="14390-104">Ajoute la personne identifiée par les paramètres _EmailAddresses_ et _DisplayName_ comme un ami pour l'utilisateur connecté sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="14390-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="14390-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14390-105">Parameters</span></span>

<span data-ttu-id="14390-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="14390-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="14390-107">dans Tableau qui contient une ou plusieurs adresses SMTP valides pour une personne sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="14390-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="14390-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="14390-108">_displayName_</span></span>
  
> <span data-ttu-id="14390-109">dans Chaîne qui contient le nom complet de la personne à ajouter en tant qu'ami.</span><span class="sxs-lookup"><span data-stu-id="14390-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14390-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="14390-110">Remarks</span></span>

<span data-ttu-id="14390-111">Si Outlook Social Connector (OSC) fournit plus de sur l'adresse SMTP dans le tableau dans le paramètre **EmailAddresses** , le fournisseur OSC peut supposer que le premier élément est l'adresse SMTP principale.</span><span class="sxs-lookup"><span data-stu-id="14390-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="14390-112">Si le fournisseur a défini l'élément **followPerson** comme **true** dans les **fonctionnalités** XML et qu'aucun des éléments de _EmailAddresses_ ne correspond à un utilisateur sur le réseau, le fournisseur doit renvoyer l'erreur OSC_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="14390-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="14390-113">Si le fournisseur a défini **followPerson** comme **false** dans les **fonctionnalités**, le fournisseur doit renvoyer l'erreur OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="14390-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="14390-114">Si la méthode **FollowPersonEx** réussit, le fournisseur peut utiliser la chaîne dans le paramètre _DisplayName_ pour adresser la personne dans tout message électronique de confirmation Friend suivant, au lieu de l'adresser par l'adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="14390-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="14390-115">En revanche, le fournisseur doit être en mesure de gérer le OSC en passant une chaîne vide pour le paramètre _DisplayName_ .</span><span class="sxs-lookup"><span data-stu-id="14390-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="14390-116">Si le fournisseur implémente l'interface [ISocialSession2](isocialsession2iunknown.md) et a défini **followPerson** sur **true** dans les fonctionnalités XML, l'interface OSC appelle **FollowPersonEx** au lieu de [ISocialSession:: followPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="14390-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="14390-117">Si le fournisseur a défini **followPerson** comme **true** mais n'implémente pas l'interface **ISocialSession2** , ou **FollowPersonEx** renvoie l'erreur OSC_E_NOTIMPL, l'interface OSC appelle **ISocialSession:: followPerson**.</span><span class="sxs-lookup"><span data-stu-id="14390-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="14390-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14390-118">See also</span></span>

- [<span data-ttu-id="14390-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14390-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

