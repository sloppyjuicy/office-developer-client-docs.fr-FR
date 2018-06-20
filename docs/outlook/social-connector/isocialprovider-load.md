---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Initialise le fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: 172595db8d9467f22a80c8caf0e3444250826aaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787600"
---
# <a name="isocialproviderload"></a><span data-ttu-id="301d2-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="301d2-103">ISocialProvider::Load</span></span>

<span data-ttu-id="301d2-104">Initialise le fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="301d2-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="301d2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="301d2-105">Parameters</span></span>

<span data-ttu-id="301d2-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="301d2-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="301d2-107">[in] La version des interfaces de fournisseur OSC attendue par le OSC.</span><span class="sxs-lookup"><span data-stu-id="301d2-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="301d2-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="301d2-108">_languageTag_</span></span>
  
> <span data-ttu-id="301d2-109">[in] La balise de langue Internet Engineering Task Force (IETF), définie par la [[norme RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), qui représente la langue d’interface utilisateur Outlook active.</span><span class="sxs-lookup"><span data-stu-id="301d2-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="301d2-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="301d2-110">Remarks</span></span>

<span data-ttu-id="301d2-111">Le format de version pour le paramètre _socialProviderInterfaceVersion_ est _X_. _xxxx_, où _X_ est la version principale et _xxxx_ est la version secondaire de la OSC.</span><span class="sxs-lookup"><span data-stu-id="301d2-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="301d2-112">Pour Office 2013, recherchez la version principale est 15.</span><span class="sxs-lookup"><span data-stu-id="301d2-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="301d2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="301d2-113">See also</span></span>

- [<span data-ttu-id="301d2-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="301d2-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

