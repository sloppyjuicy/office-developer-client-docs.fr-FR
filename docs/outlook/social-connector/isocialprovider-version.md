---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Renvoie une chaîne qui représente le numéro de version du fournisseur pour ce réseau social.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438273"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="cf35c-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="cf35c-103">ISocialProvider::Version</span></span>

<span data-ttu-id="cf35c-104">Renvoie une chaîne qui représente le numéro de version du fournisseur pour ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="cf35c-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="cf35c-105">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cf35c-105">Property value</span></span>

<span data-ttu-id="cf35c-106">Chaîne qui contient le numéro de version du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="cf35c-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf35c-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf35c-107">Remarks</span></span>

<span data-ttu-id="cf35c-108">La chaîne de version doit utiliser  _la version MajeureVersion_.</span><span class="sxs-lookup"><span data-stu-id="cf35c-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="cf35c-109">_Format MinorVersion_ (par exemple, 1,4730).</span><span class="sxs-lookup"><span data-stu-id="cf35c-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf35c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf35c-110">See also</span></span>

- [<span data-ttu-id="cf35c-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf35c-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

