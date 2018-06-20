---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787588"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="6247f-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="6247f-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="6247f-104">Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="6247f-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="6247f-105">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="6247f-105">Property value</span></span>

<span data-ttu-id="6247f-106">Pointeur vers une structure qui spécifie un tableau de chaînes qui représentent les URL des sites pour le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="6247f-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6247f-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="6247f-107">Remarks</span></span>

<span data-ttu-id="6247f-108">Un fournisseur peut prendre en charge plusieurs URL des sites.</span><span class="sxs-lookup"><span data-stu-id="6247f-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="6247f-109">L’OSC définit la propriété [ISocialSession::SiteUrl](isocialsession-siteurl.md) pour informer le fournisseur de l’URL du site sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6247f-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="6247f-110">L’OSC utilise le premier élément du tableau en tant que l’URL du site par défaut.</span><span class="sxs-lookup"><span data-stu-id="6247f-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="6247f-111">Un fournisseur peut retourner des éléments supplémentaires dans le tableau d’URL de site, mais l’OSC ne les utilise pas.</span><span class="sxs-lookup"><span data-stu-id="6247f-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6247f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6247f-112">See also</span></span>

- [<span data-ttu-id="6247f-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6247f-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

