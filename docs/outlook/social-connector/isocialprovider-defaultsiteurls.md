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
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Renvoie un tableau de chaînes qui spécifient les URL de site pour le fournisseur Outlook Social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Valeur de propriété

Pointeur vers une structure qui spécifie un tableau de chaînes qui représentent les URL des sites pour le fournisseur OSC.
  
## <a name="remarks"></a>Remarques

Un fournisseur peut prendre en charge plusieurs URL des sites. L’OSC définit la propriété [ISocialSession::SiteUrl](isocialsession-siteurl.md) pour informer le fournisseur de l’URL du site sélectionné. 
  
L’OSC utilise le premier élément du tableau en tant que l’URL du site par défaut. Un fournisseur peut retourner des éléments supplémentaires dans le tableau d’URL de site, mais l’OSC ne les utilise pas. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

