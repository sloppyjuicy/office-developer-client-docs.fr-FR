---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Ouvre une session sur le site de réseau social à l’aide de l’authentification basée sur les formulaires.
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787618"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="34738-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="34738-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="34738-104">Ouvre une session sur le site de réseau social à l’aide de l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="34738-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="34738-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34738-105">Parameters</span></span>

<span data-ttu-id="34738-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="34738-106">_connectIn_</span></span>
  
> <span data-ttu-id="34738-107">[in] Chaîne qui est **null**, une URL à un formulaire d’ouverture de session sur le site web ou une chaîne qui contient les informations d’identification d’ouverture de session, selon le contexte du processus d’ouverture de session lorsque cette méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="34738-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="34738-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="34738-108">_connectOut_</span></span>
  
> <span data-ttu-id="34738-109">[out] Chaîne qui contient les informations d’identification d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="34738-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34738-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="34738-110">Remarks</span></span>

<span data-ttu-id="34738-111">L’Outlook Social Connector (OSC) appelle la méthode **LogonWeb** uniquement si le fournisseur indique qu’il prend en charge l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="34738-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="34738-112">Le fournisseur indique qu’il exige l’authentification basée sur les formulaires en définissant **useLogonWebAuth** comme **true** dans le code XML des **capacités**.</span><span class="sxs-lookup"><span data-stu-id="34738-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="34738-113">Si le fournisseur définit **useLogonWebAuth** comme **false**, l’OSC utilise l’authentification de base et appelle la méthode [ISocialSession::Logon](isocialsession-logon.md) .</span><span class="sxs-lookup"><span data-stu-id="34738-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="34738-114">Se connecter à un site de réseau social à l’aide de l’authentification basée sur les formulaires implique d’appeler les méthodes **LogonWeb** et [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) dans un ordre spécifique :</span><span class="sxs-lookup"><span data-stu-id="34738-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="34738-115">L’OSC appelle **LogonWeb** la première fois, en passant **null** au paramètre _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="34738-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="34738-116">Le fournisseur génère l’erreur OSC_E_AUTH_ERROR à l’OSC.</span><span class="sxs-lookup"><span data-stu-id="34738-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="34738-117">L’OSC appelle ensuite **GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="34738-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="34738-118">Le fournisseur renvoie l’URL appropriée à une page d’ouverture de session dans la méthode **GetLogonUrl** .</span><span class="sxs-lookup"><span data-stu-id="34738-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="34738-119">L’OSC utilise l’URL renvoyée par **GetLogonUrl** pour afficher la page d’ouverture de session basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="34738-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="34738-120">L’OSC appelle ensuite **LogonWeb** une deuxième fois, en transmettant l’URL du formulaire d’ouverture de session dans le paramètre _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="34738-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="34738-121">Si l’authentification réussit, le fournisseur retourne les informations d’identification d’ouverture de session dans le paramètre _connectOut_ à l’OSC.</span><span class="sxs-lookup"><span data-stu-id="34738-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="34738-122">Si l’authentification échoue, le fournisseur déclenche l’erreur OSC_E_AUTH_ERROR à l’OSC.</span><span class="sxs-lookup"><span data-stu-id="34738-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="34738-123">Si le fournisseur OSC prend en charge la connexion à l’aide des informations d’identification mises en cache, il spécifie **useLogonCached** comme **true** dans le XML des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="34738-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="34738-124">Le fournisseur doit placer les informations d’identification d’ouverture de session dans la chaîne _connectOut_ que le fournisseur souhaite l’OSC pour stocker les connexions.</span><span class="sxs-lookup"><span data-stu-id="34738-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="34738-125">L’OSC n’interprète pas la chaîne _connectOut_ .</span><span class="sxs-lookup"><span data-stu-id="34738-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="34738-126">Une fois l’OSC vérifie **useLogonCached** a la **valeur true**, l’OSC chiffre la chaîne pour la sécurité avant de les stocker dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="34738-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="34738-127">L’OSC transmet cette chaîne au paramètre _connectIn_ lors des tentatives suivantes pour vous connecter au réseau social en appelant [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span><span class="sxs-lookup"><span data-stu-id="34738-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="34738-128">Pour plus d’informations sur les codes d’erreur, voir [Codes d’erreur de fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="34738-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34738-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34738-129">See also</span></span>

- [<span data-ttu-id="34738-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34738-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="34738-131">Authentification basée sur les formulaires</span><span class="sxs-lookup"><span data-stu-id="34738-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

