---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtient une valeur de type String qui représente une URL utilisée pour présenter un formulaire basé sur un navigateur à l'utilisateur lors de l'authentification Web.
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285377"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="7bb95-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="7bb95-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="7bb95-104">Obtient une valeur de type String qui représente une URL utilisée pour présenter un formulaire basé sur un navigateur à l'utilisateur lors de l'authentification Web.</span><span class="sxs-lookup"><span data-stu-id="7bb95-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="7bb95-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7bb95-105">Parameters</span></span>

<span data-ttu-id="7bb95-106">_url_</span><span class="sxs-lookup"><span data-stu-id="7bb95-106">_url_</span></span>
  
> <span data-ttu-id="7bb95-107">remarquer Chaîne qui contient une URL pour le formulaire utilisé dans l'authentification Web.</span><span class="sxs-lookup"><span data-stu-id="7bb95-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7bb95-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="7bb95-108">Remarks</span></span>

<span data-ttu-id="7bb95-109">Une fois que le formulaire est présenté à l'utilisateur, la méthode [ISocialSession:: LogonWeb](isocialsession-logonweb.md) est appelée avec une chaîne vide pour le paramètre _Connect_ .</span><span class="sxs-lookup"><span data-stu-id="7bb95-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7bb95-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bb95-110">See also</span></span>

- [<span data-ttu-id="7bb95-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7bb95-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

