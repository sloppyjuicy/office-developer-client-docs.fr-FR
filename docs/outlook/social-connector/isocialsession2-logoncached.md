---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Ouvre une session sur le site de réseau social à l’aide des informations d’identification mises en cache.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787625"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="c6420-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="c6420-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="c6420-104">Ouvre une session sur le site de réseau social à l’aide des informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="c6420-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="c6420-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6420-105">Parameters</span></span>

<span data-ttu-id="c6420-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="c6420-106">_connectIn_</span></span>
  
> <span data-ttu-id="c6420-107">[in] Chaîne qui peut être vide ou contient les informations d’identification d’ouverture de session, selon le contexte dans lequel l’OSC appelle **LogonCached**.</span><span class="sxs-lookup"><span data-stu-id="c6420-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="c6420-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="c6420-108">_userName_</span></span>
  
> <span data-ttu-id="c6420-109">[in] Chaîne qui contient le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6420-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="c6420-110">_mot de passe_</span><span class="sxs-lookup"><span data-stu-id="c6420-110">_password_</span></span>
  
> <span data-ttu-id="c6420-111">[in] Chaîne qui contient le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="c6420-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="c6420-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="c6420-112">_connectOut_</span></span>
  
> <span data-ttu-id="c6420-113">[out] Une chaîne opaque qui contient les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c6420-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6420-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6420-114">Remarks</span></span>

<span data-ttu-id="c6420-115">Cette méthode est appelée pour l’authentification uniquement si **useLogonCached** est définie comme **true** dans le XML des **fonctionnalités** renvoyé par [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span><span class="sxs-lookup"><span data-stu-id="c6420-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="c6420-116">L’Outlook Social Connector (OSC) appelle **LogonCached**et transmet une chaîne vide pour _connectIn_ et chaînes de _nom d’utilisateur_ et _mot de passe_ non vide.</span><span class="sxs-lookup"><span data-stu-id="c6420-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="c6420-117">Le fournisseur utilise le _nom d’utilisateur_ et _mot de passe_ pour vous connecter au réseau social et retourne un paramètre opaque _connectOut_ à l’OSC si l’authentification réussit.</span><span class="sxs-lookup"><span data-stu-id="c6420-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="c6420-118">Si l’authentification échoue, le fournisseur renvoie l’erreur OSC_E_LOGON_FAILURE à l’OSC.</span><span class="sxs-lookup"><span data-stu-id="c6420-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="c6420-119">Le paramètre _connectOut_ est une chaîne opaque à l’OSC et est transmis au paramètre _connectIn_ lors des tentatives suivantes à l’OSC à se connecter au réseau social.</span><span class="sxs-lookup"><span data-stu-id="c6420-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="c6420-120">Le fournisseur doit placer les informations d’identification dans la chaîne _connectOut_ que le fournisseur souhaite l’OSC pour stocker les connexions.</span><span class="sxs-lookup"><span data-stu-id="c6420-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="c6420-121">L’OSC n’interprète pas la chaîne de _connectOut_et chiffre la chaîne pour des raisons de sécurité avant de les stocker dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="c6420-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6420-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6420-122">See also</span></span>

- [<span data-ttu-id="c6420-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6420-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

