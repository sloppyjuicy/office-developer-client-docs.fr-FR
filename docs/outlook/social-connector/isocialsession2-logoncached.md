---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Se connecte au site de réseau social à l’aide des informations d’identification mises en cache.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436621"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="6127e-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="6127e-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="6127e-104">Se connecte au site de réseau social à l’aide des informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="6127e-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="6127e-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="6127e-105">Parameters</span></span>

<span data-ttu-id="6127e-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="6127e-106">_connectIn_</span></span>
  
> <span data-ttu-id="6127e-107">[in] Chaîne qui peut être vide ou qui contient les informations d’identification de connexion, selon le contexte dans lequel OSC appelle **LogonCached**.</span><span class="sxs-lookup"><span data-stu-id="6127e-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="6127e-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="6127e-108">_userName_</span></span>
  
> <span data-ttu-id="6127e-109">[in] Chaîne qui contient le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6127e-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="6127e-110">_mot de passe_</span><span class="sxs-lookup"><span data-stu-id="6127e-110">_password_</span></span>
  
> <span data-ttu-id="6127e-111">[in] Chaîne qui contient le mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6127e-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="6127e-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="6127e-112">_connectOut_</span></span>
  
> <span data-ttu-id="6127e-113">[out] Chaîne opaque qui contient des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="6127e-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6127e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6127e-114">Remarks</span></span>

<span data-ttu-id="6127e-115">Cette méthode est appelée pour l’authentification uniquement si **useLogonCached** est définie comme **true** dans les fonctionnalités **XML** renvoyées par [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span><span class="sxs-lookup"><span data-stu-id="6127e-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="6127e-116">Le Outlook Social Connector (OSC) appelle **LogonCached** et transmet une chaîne vide pour les chaînes _connectIn_ et _userName_ et _password_ non vides.</span><span class="sxs-lookup"><span data-stu-id="6127e-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="6127e-117">Le fournisseur utilise _userName_ et le mot de passe pour se connecter au réseau social et renvoie un paramètre _opaque connectOut_ à l’OSC si l’authentification réussit. </span><span class="sxs-lookup"><span data-stu-id="6127e-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="6127e-118">En cas d’échec de l’authentification, le fournisseur renvoie OSC_E_LOGON_FAILURE erreur de message à l’OSC.</span><span class="sxs-lookup"><span data-stu-id="6127e-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="6127e-119">Le  _paramètre connectOut_ est une chaîne opaque à OSC et est transmis au paramètre  _connectIn_ lors des tentatives ultérieures de connexion au réseau social par l’OSC.</span><span class="sxs-lookup"><span data-stu-id="6127e-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="6127e-120">Le fournisseur doit placer toutes les informations d’identification dans la  _chaîne connectOut_ que le fournisseur souhaite que l’OSC stocke sur plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="6127e-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="6127e-121">L’OSC n’interprète pas la chaîne dans _connectOut_ et chiffre la chaîne à des fins de sécurité avant de la stocker dans Windows registre.</span><span class="sxs-lookup"><span data-stu-id="6127e-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6127e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6127e-122">See also</span></span>

- [<span data-ttu-id="6127e-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6127e-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

