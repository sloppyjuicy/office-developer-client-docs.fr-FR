---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: Ouvre une session sur le site de réseau social à l’aide du nom d’utilisateur et le mot de passe.
ms.openlocfilehash: d7a79767f3726f9748ea48839f1e190af2e9ec74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787613"
---
# <a name="isocialsessionlogon"></a><span data-ttu-id="102aa-103">ISocialSession::Logon</span><span class="sxs-lookup"><span data-stu-id="102aa-103">ISocialSession::Logon</span></span>

<span data-ttu-id="102aa-104">Ouvre une session sur le site de réseau social à l’aide du nom d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="102aa-104">Logs on to the social network site by using the specified user name and password.</span></span>
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a><span data-ttu-id="102aa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="102aa-105">Parameters</span></span>

<span data-ttu-id="102aa-106">_nom d’utilisateur_</span><span class="sxs-lookup"><span data-stu-id="102aa-106">_username_</span></span>
  
> <span data-ttu-id="102aa-107">[in] Chaîne qui contient le nom d’utilisateur à se connecter.</span><span class="sxs-lookup"><span data-stu-id="102aa-107">[in] A string that contains the user name to log on.</span></span>
    
<span data-ttu-id="102aa-108">_mot de passe_</span><span class="sxs-lookup"><span data-stu-id="102aa-108">_password_</span></span>
  
> <span data-ttu-id="102aa-109">[in] Chaîne qui contient le mot de passe pour vous connecter.</span><span class="sxs-lookup"><span data-stu-id="102aa-109">[in] A string that contains the password to log on.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="102aa-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="102aa-110">See also</span></span>

- [<span data-ttu-id="102aa-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="102aa-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

