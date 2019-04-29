---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Ouvre une session sur le site réseau social à l'aide des informations d'identification mises en cache.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436621"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="2ae22-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="2ae22-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="2ae22-104">Ouvre une session sur le site réseau social à l'aide des informations d'identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="2ae22-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="2ae22-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ae22-105">Parameters</span></span>

<span data-ttu-id="2ae22-106">_connexion_</span><span class="sxs-lookup"><span data-stu-id="2ae22-106">_connectIn_</span></span>
  
> <span data-ttu-id="2ae22-107">dans Une chaîne qui peut être vide ou qui contient les informations d'identification de connexion, en fonction du contexte dans lequel OSC appelle **LogonCached**.</span><span class="sxs-lookup"><span data-stu-id="2ae22-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="2ae22-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="2ae22-108">_userName_</span></span>
  
> <span data-ttu-id="2ae22-109">dans Chaîne qui contient le nom d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ae22-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="2ae22-110">_mot de passe_</span><span class="sxs-lookup"><span data-stu-id="2ae22-110">_password_</span></span>
  
> <span data-ttu-id="2ae22-111">dans Chaîne qui contient le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ae22-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="2ae22-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="2ae22-112">_connectOut_</span></span>
  
> <span data-ttu-id="2ae22-113">remarquer Chaîne opaque qui contient les informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="2ae22-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ae22-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2ae22-114">Remarks</span></span>

<span data-ttu-id="2ae22-115">Cette méthode est appelée pour l'authentification uniquement si **useLogonCached** est défini sur **true** dans les **fonctionnalités** XML renvoyées par [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md).</span><span class="sxs-lookup"><span data-stu-id="2ae22-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="2ae22-116">Outlook Social Connector (OSC) appelle **LogonCached**et transmet une chaîne vide pour les chaînes de _nom d'utilisateur_ et _de mot de passe_ de _connexion_ et non vide.</span><span class="sxs-lookup"><span data-stu-id="2ae22-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="2ae22-117">Le fournisseur utilise le _nom d'utilisateur_ et le _mot de passe_ pour se connecter au réseau social et renvoie un paramètre _connectOut_ opaque à OSC si l'authentification réussit.</span><span class="sxs-lookup"><span data-stu-id="2ae22-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="2ae22-118">Si l'authentification échoue, le fournisseur renvoie l'erreur OSC_E_LOGON_FAILURE au OSC.</span><span class="sxs-lookup"><span data-stu-id="2ae22-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="2ae22-119">Le paramètre _connectOut_ est une chaîne opaque vers OSC, et est transmis au paramètre _Connect_ sur les tentatives suivantes de l'OSC pour se connecter au réseau social.</span><span class="sxs-lookup"><span data-stu-id="2ae22-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="2ae22-120">Le fournisseur doit placer toutes les informations d'identification dans la chaîne _connectOut_ que le fournisseur souhaite que OSC stocke sur les connexions.</span><span class="sxs-lookup"><span data-stu-id="2ae22-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="2ae22-121">Le OSC n'interprète pas la chaîne dans _connectOut_et chiffre la chaîne à des fins de sécurité avant de la stocker dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="2ae22-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2ae22-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ae22-122">See also</span></span>

- [<span data-ttu-id="2ae22-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ae22-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

