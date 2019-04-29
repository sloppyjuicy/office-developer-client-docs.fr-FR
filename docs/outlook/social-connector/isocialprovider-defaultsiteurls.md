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
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur Outlook Social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une structure qui spécifie un tableau de chaînes qui représentent les URL de site pour le fournisseur OSC.
  
## <a name="remarks"></a>Remarques

Un fournisseur peut prendre en charge plusieurs URL de site. Le OSC définit la propriété [ISocialSession:: SiteUrl](isocialsession-siteurl.md) pour informer le fournisseur de l'URL de site sélectionnée. 
  
Le OSC utilise le premier élément du tableau comme URL de site par défaut. Un fournisseur peut renvoyer des éléments supplémentaires dans le tableau d'URL du site, mais le OSC ne les utilise pas. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

