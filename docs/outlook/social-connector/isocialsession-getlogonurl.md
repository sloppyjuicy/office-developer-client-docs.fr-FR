---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtient une chaîne qui représente une URL qui est utilisée pour présenter un formulaire basé sur un navigateur à l’utilisateur lors de l’authentification web.
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787605"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="0e170-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="0e170-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="0e170-104">Obtient une chaîne qui représente une URL qui est utilisée pour présenter un formulaire basé sur un navigateur à l’utilisateur lors de l’authentification web.</span><span class="sxs-lookup"><span data-stu-id="0e170-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="0e170-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e170-105">Parameters</span></span>

<span data-ttu-id="0e170-106">_URL_</span><span class="sxs-lookup"><span data-stu-id="0e170-106">_url_</span></span>
  
> <span data-ttu-id="0e170-107">[out] Chaîne qui contient une URL pour le formulaire utilisé dans l’authentification web.</span><span class="sxs-lookup"><span data-stu-id="0e170-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e170-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e170-108">Remarks</span></span>

<span data-ttu-id="0e170-109">Une fois que le formulaire est présenté à l’utilisateur, la méthode [ISocialSession::LogonWeb](isocialsession-logonweb.md) est appelée avec une chaîne vide pour le paramètre _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="0e170-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e170-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e170-110">See also</span></span>

- [<span data-ttu-id="0e170-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e170-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

