---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Ouvre une session sur le site réseau social à l'aide de l'authentification basée sur les formulaires.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335363"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="aed0a-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="aed0a-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="aed0a-104">Ouvre une session sur le site réseau social à l'aide de l'authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="aed0a-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="aed0a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aed0a-105">Parameters</span></span>

<span data-ttu-id="aed0a-106">_connexion_</span><span class="sxs-lookup"><span data-stu-id="aed0a-106">_connectIn_</span></span>
  
> <span data-ttu-id="aed0a-107">dans Une chaîne qui est **null**, une URL vers un formulaire de connexion sur le Web ou une chaîne qui contient les informations d'identification de connexion, en fonction du contexte dans le processus d'ouverture de session lors de l'appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="aed0a-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="aed0a-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="aed0a-108">_connectOut_</span></span>
  
> <span data-ttu-id="aed0a-109">remarquer Chaîne qui contient les informations d'identification d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="aed0a-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aed0a-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="aed0a-110">Remarks</span></span>

<span data-ttu-id="aed0a-111">Outlook Social Connector (OSC) appelle la méthode **LogonWeb** uniquement si le fournisseur indique qu'il prend en charge l'authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="aed0a-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="aed0a-112">Le fournisseur indique qu'il nécessite l'authentification basée sur les formulaires en définissant **useLogonWebAuth** comme **true** dans le code XML pour les **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="aed0a-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="aed0a-113">Si le fournisseur définit **useLogonWebAuth** comme **false**, le OSC utilise l'authentification de base et appelle la méthode [ISocialSession:: Logon](isocialsession-logon.md) .</span><span class="sxs-lookup"><span data-stu-id="aed0a-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="aed0a-114">La connexion à un site de réseau social à l'aide de l'authentification basée sur les formulaires implique l'appel des méthodes **LogonWeb** et [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) dans un ordre spécifique:</span><span class="sxs-lookup"><span data-stu-id="aed0a-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="aed0a-115">Le OSC appelle **LogonWeb** la première fois, en transmettant la **valeur null** au paramètre _Connect_ .</span><span class="sxs-lookup"><span data-stu-id="aed0a-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="aed0a-116">Le fournisseur déclenche l'erreur OSC_E_AUTH_ERROR au OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0a-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="aed0a-117">Le OSC appelle ensuite **GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="aed0a-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="aed0a-118">Le fournisseur renvoie l'URL appropriée à une page de connexion dans la méthode **GetLogonUrl** .</span><span class="sxs-lookup"><span data-stu-id="aed0a-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="aed0a-119">Le OSC utilise l'URL renvoyée par **GetLogonUrl** pour afficher la page d'ouverture de session basée sur des formulaires.</span><span class="sxs-lookup"><span data-stu-id="aed0a-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="aed0a-120">Le OSC appelle ensuite **LogonWeb** une deuxième fois, en transmettant l'URL au formulaire d'ouverture de session dans le paramètre _Connect_ .</span><span class="sxs-lookup"><span data-stu-id="aed0a-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="aed0a-121">Si l'authentification réussit, le fournisseur renvoie les informations d'identification d'ouverture de session dans le paramètre _connectOut_ dans le OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0a-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="aed0a-122">Si l'authentification échoue, le fournisseur déclenche l'erreur OSC_E_AUTH_ERROR au OSC.</span><span class="sxs-lookup"><span data-stu-id="aed0a-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="aed0a-123">Si le fournisseur OSC prend en charge l'ouverture de session à l'aide des informations d'identification mises en cache, il spécifie **useLogonCached** comme **true** dans les **fonctionnalités** XML.</span><span class="sxs-lookup"><span data-stu-id="aed0a-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="aed0a-124">Le fournisseur doit placer toutes les informations d'identification d'ouverture de session dans la chaîne _connectOut_ que le fournisseur veut que OSC stocke sur les connexions.</span><span class="sxs-lookup"><span data-stu-id="aed0a-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="aed0a-125">Le OSC n'interprète pas la chaîne _connectOut_ .</span><span class="sxs-lookup"><span data-stu-id="aed0a-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="aed0a-126">Une fois que le contrôle OSC a vérifié que **useLogonCached** a la **valeur true**, le contrôle OSC chiffre la chaîne à des fins de sécurité avant de la stocker dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="aed0a-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="aed0a-127">L'OSC transmet cette chaîne au paramètre _Connect_ lors des tentatives suivantes de connexion au réseau social en appelant [ISocialSession2:: LogonCached](isocialsession2-logoncached.md).</span><span class="sxs-lookup"><span data-stu-id="aed0a-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="aed0a-128">Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="aed0a-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aed0a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aed0a-129">See also</span></span>

- [<span data-ttu-id="aed0a-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aed0a-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="aed0a-131">Authentification basée sur les formulaires</span><span class="sxs-lookup"><span data-stu-id="aed0a-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

