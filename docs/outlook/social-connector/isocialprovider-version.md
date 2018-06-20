---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Renvoie une chaîne qui représente le numéro de version du fournisseur de ce réseau social.
ms.openlocfilehash: 5c82df2dc4c052b1a06bcecb16defbb4dee38b18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787603"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="8e657-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="8e657-103">ISocialProvider::Version</span></span>

<span data-ttu-id="8e657-104">Renvoie une chaîne qui représente le numéro de version du fournisseur de ce réseau social.</span><span class="sxs-lookup"><span data-stu-id="8e657-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="8e657-105">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="8e657-105">Property value</span></span>

<span data-ttu-id="8e657-106">Chaîne qui contient le numéro de version du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8e657-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e657-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e657-107">Remarks</span></span>

<span data-ttu-id="8e657-108">La chaîne de version doit utiliser le _MajorVersion_.</span><span class="sxs-lookup"><span data-stu-id="8e657-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="8e657-109">Format _MinorVersion_ (par exemple, 1.4730).</span><span class="sxs-lookup"><span data-stu-id="8e657-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e657-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e657-110">See also</span></span>

- [<span data-ttu-id="8e657-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e657-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

