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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285758"
---
# <a name="isocialproviderload"></a><span data-ttu-id="c1b02-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="c1b02-103">ISocialProvider::Load</span></span>

<span data-ttu-id="c1b02-104">Initialise le fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="c1b02-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="c1b02-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1b02-105">Parameters</span></span>

<span data-ttu-id="c1b02-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="c1b02-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="c1b02-107">[in] Version des interfaces du fournisseur OSC attendues par l’OSC.</span><span class="sxs-lookup"><span data-stu-id="c1b02-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="c1b02-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="c1b02-108">_languageTag_</span></span>
  
> <span data-ttu-id="c1b02-109">[in] Balise de langue IETF (Internet Engineering Task Force), définie par [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) et [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)qui représente la langue actuelle de l’interface utilisateur Outlook.</span><span class="sxs-lookup"><span data-stu-id="c1b02-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1b02-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1b02-110">Remarks</span></span>

<span data-ttu-id="c1b02-111">Le format de version du  _paramètre socialProviderInterfaceVersion_ est  _X_. _xxxx_, où  _X_ est la version principale et  _xxxx_ la version mineure de l’OSC.</span><span class="sxs-lookup"><span data-stu-id="c1b02-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="c1b02-112">Pour Office 2013, vérifiez que la version principale est 15.</span><span class="sxs-lookup"><span data-stu-id="c1b02-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1b02-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b02-113">See also</span></span>

- [<span data-ttu-id="c1b02-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1b02-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

