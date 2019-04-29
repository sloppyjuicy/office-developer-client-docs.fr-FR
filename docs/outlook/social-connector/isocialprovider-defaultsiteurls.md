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
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413772"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="06233-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="06233-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="06233-104">Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="06233-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="06233-105">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="06233-105">Property value</span></span>

<span data-ttu-id="06233-106">Pointeur vers une structure qui spécifie un tableau de chaînes qui représentent les URL de site pour le fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="06233-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06233-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="06233-107">Remarks</span></span>

<span data-ttu-id="06233-108">Un fournisseur peut prendre en charge plusieurs URL de site.</span><span class="sxs-lookup"><span data-stu-id="06233-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="06233-109">Le OSC définit la propriété [ISocialSession:: SiteUrl](isocialsession-siteurl.md) pour informer le fournisseur de l'URL de site sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="06233-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="06233-110">Le OSC utilise le premier élément du tableau comme URL de site par défaut.</span><span class="sxs-lookup"><span data-stu-id="06233-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="06233-111">Un fournisseur peut renvoyer des éléments supplémentaires dans le tableau d'URL du site, mais le OSC ne les utilise pas.</span><span class="sxs-lookup"><span data-stu-id="06233-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06233-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06233-112">See also</span></span>

- [<span data-ttu-id="06233-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="06233-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

