---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Renvoie une valeur de type String qui représente le numéro de version du fournisseur de ce réseau social.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285384"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="5c384-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="5c384-103">ISocialProvider::Version</span></span>

<span data-ttu-id="5c384-104">Renvoie une valeur de type String qui représente le numéro de version du fournisseur de ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="5c384-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="5c384-105">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5c384-105">Property value</span></span>

<span data-ttu-id="5c384-106">Chaîne qui contient le numéro de version du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5c384-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c384-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c384-107">Remarks</span></span>

<span data-ttu-id="5c384-108">La chaîne de version doit utiliser la version _MajorVersion_.</span><span class="sxs-lookup"><span data-stu-id="5c384-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="5c384-109">Format _MinorVersion_ (par exemple, 1,4730).</span><span class="sxs-lookup"><span data-stu-id="5c384-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c384-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c384-110">See also</span></span>

- [<span data-ttu-id="5c384-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c384-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

