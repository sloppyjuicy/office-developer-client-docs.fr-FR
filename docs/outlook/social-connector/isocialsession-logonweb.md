---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Se connecte au site de réseau social à l’aide de l’authentification basée sur les formulaires.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430335"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="66bdd-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="66bdd-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="66bdd-104">Se connecte au site de réseau social à l’aide de l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="66bdd-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="66bdd-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="66bdd-105">Parameters</span></span>

<span data-ttu-id="66bdd-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="66bdd-106">_connectIn_</span></span>
  
> <span data-ttu-id="66bdd-107">[in] Chaîne **null,** URL d’un formulaire de connexion sur le web ou chaîne qui contient les informations d’identification de connexion, selon le contexte du processus d’connexion lorsque cette méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="66bdd-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="66bdd-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="66bdd-108">_connectOut_</span></span>
  
> <span data-ttu-id="66bdd-109">[out] Chaîne qui contient les informations d’identification de connexion.</span><span class="sxs-lookup"><span data-stu-id="66bdd-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66bdd-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="66bdd-110">Remarks</span></span>

<span data-ttu-id="66bdd-111">Le Outlook Social Connector (OSC) appelle la méthode **LogonWeb** uniquement si le fournisseur indique qu’il prend en charge l’authentification basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="66bdd-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="66bdd-112">Le fournisseur indique qu’il requiert une authentification basée sur les formulaires en étiquetant **useLogonWebAuth** comme **vrai** dans le XML pour **les fonctionnalités.**</span><span class="sxs-lookup"><span data-stu-id="66bdd-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="66bdd-113">Si le fournisseur définit **useLogonWebAuth** comme **false,** l’OSC utilise l’authentification de base et appelle la [méthode ISocialSession::Logon.](isocialsession-logon.md)</span><span class="sxs-lookup"><span data-stu-id="66bdd-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="66bdd-114">La connexion à un site de réseau social à l’aide de l’authentification basée sur les formulaires implique l’appel des méthodes **LogonWeb** et [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) dans un ordre spécifique :</span><span class="sxs-lookup"><span data-stu-id="66bdd-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="66bdd-115">L’OSC appelle **LogonWeb** la première fois, en passant la valeur **null** au _paramètre connectIn._</span><span class="sxs-lookup"><span data-stu-id="66bdd-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="66bdd-116">Le fournisseur lève l’erreur OSC_E_AUTH_ERROR à l’OSC.</span><span class="sxs-lookup"><span data-stu-id="66bdd-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="66bdd-117">L’OSC appelle ensuite **GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="66bdd-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="66bdd-118">Le fournisseur renvoie l’URL appropriée à une page d’accès dans la **méthode GetLogonUrl.**</span><span class="sxs-lookup"><span data-stu-id="66bdd-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="66bdd-119">L’OSC utilise l’URL renvoyée par **GetLogonUrl** pour afficher la page d’inscription basée sur les formulaires.</span><span class="sxs-lookup"><span data-stu-id="66bdd-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="66bdd-120">L’OSC appelle ensuite **LogonWeb** une deuxième fois, en passant l’URL au formulaire de connexion dans le _paramètre connectIn._</span><span class="sxs-lookup"><span data-stu-id="66bdd-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="66bdd-121">Si l’authentification réussit, le fournisseur renvoie les informations d’identification de connexion dans le  _paramètre connectOut_ à l’OSC.</span><span class="sxs-lookup"><span data-stu-id="66bdd-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="66bdd-122">En cas d’échec de l’authentification, le fournisseur OSC_E_AUTH_ERROR d’erreur à l’OSC.</span><span class="sxs-lookup"><span data-stu-id="66bdd-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="66bdd-123">Si le fournisseur OSC prend en charge la connexion à l’aide des informations d’identification mises en cache, il spécifie **useLogonCached** comme **true** dans le XML **des** fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="66bdd-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="66bdd-124">Le fournisseur doit placer toutes les informations d’identification de connexion dans la chaîne  _connectOut_ que le fournisseur souhaite que l’OSC stocke sur plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="66bdd-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="66bdd-125">L’OSC n’interprète pas la _chaîne connectOut._</span><span class="sxs-lookup"><span data-stu-id="66bdd-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="66bdd-126">Une fois que l’OSC a vérifié que **l’utilisation deLogonCached** est **vraie,** l’OSC chiffre la chaîne pour des raisons de sécurité avant de la stocker dans Windows registre.</span><span class="sxs-lookup"><span data-stu-id="66bdd-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="66bdd-127">L’OSC transmet cette chaîne au paramètre  _connectIn_ lors des tentatives suivantes de connexion au réseau social en appelant [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span><span class="sxs-lookup"><span data-stu-id="66bdd-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="66bdd-128">Pour plus d’informations sur les codes d’erreur, consultez la rubrique relative aux [codes d’erreur du fournisseur Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="66bdd-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66bdd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66bdd-129">See also</span></span>

- [<span data-ttu-id="66bdd-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66bdd-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="66bdd-131">Authentification basée sur les formulaires</span><span class="sxs-lookup"><span data-stu-id="66bdd-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

