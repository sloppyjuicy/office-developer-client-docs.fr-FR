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
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385829"
---
# <a name="isocialproviderload"></a><span data-ttu-id="f58f5-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="f58f5-103">ISocialProvider::Load</span></span>

<span data-ttu-id="f58f5-104">Initialise le fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="f58f5-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="f58f5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f58f5-105">Parameters</span></span>

<span data-ttu-id="f58f5-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="f58f5-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="f58f5-107">[in] La version des interfaces de fournisseur OSC attendue par le OSC.</span><span class="sxs-lookup"><span data-stu-id="f58f5-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="f58f5-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="f58f5-108">_languageTag_</span></span>
  
> <span data-ttu-id="f58f5-109">[in] La balise de langue Internet Engineering Task Force (IETF), définie par la [[norme RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), qui représente la langue d’interface utilisateur Outlook active.</span><span class="sxs-lookup"><span data-stu-id="f58f5-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f58f5-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="f58f5-110">Remarks</span></span>

<span data-ttu-id="f58f5-111">Le format de version pour le paramètre _socialProviderInterfaceVersion_ est _X_. _xxxx_, où _X_ est la version principale et _xxxx_ est la version secondaire de la OSC.</span><span class="sxs-lookup"><span data-stu-id="f58f5-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="f58f5-112">Pour Office 2013, recherchez la version principale est 15.</span><span class="sxs-lookup"><span data-stu-id="f58f5-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f58f5-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f58f5-113">See also</span></span>

- [<span data-ttu-id="f58f5-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f58f5-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

