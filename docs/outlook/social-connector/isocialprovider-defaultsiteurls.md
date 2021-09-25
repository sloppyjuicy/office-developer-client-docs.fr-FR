---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur Outlook Social Connector (OSC).
ms.openlocfilehash: bbdd30265c45ea140361149ecc97f5678beb54b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629143"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur Outlook Social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une structure qui spécifie un tableau de chaînes qui représentent les URL de site pour le fournisseur OSC.
  
## <a name="remarks"></a>Remarques

Un fournisseur peut prendre en charge plusieurs URL de site. L’OSC définit la [propriété ISocialSession::SiteUrl](isocialsession-siteurl.md) pour informer le fournisseur de l’URL du site sélectionné. 
  
L’OSC utilise le premier élément du tableau comme URL de site par défaut. Un fournisseur peut renvoyer des éléments supplémentaires dans le tableau d’URL du site, mais l’OSC ne les utilise pas. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

