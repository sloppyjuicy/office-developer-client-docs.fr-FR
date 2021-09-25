---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Renvoie une chaîne qui représente le numéro de version du fournisseur pour ce réseau social.
ms.openlocfilehash: 5f3e285d4a22f667eaef6008982057673dfcbcd0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629122"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Renvoie une chaîne qui représente le numéro de version du fournisseur pour ce réseau social. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient le numéro de version du fournisseur.
  
## <a name="remarks"></a>Remarques

La chaîne de version doit utiliser  _la version MajeureVersion_. _Format MinorVersion_ (par exemple, 1,4730). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

