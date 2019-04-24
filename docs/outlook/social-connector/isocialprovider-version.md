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
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Renvoie une valeur de type String qui représente le numéro de version du fournisseur de ce réseau social. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient le numéro de version du fournisseur.
  
## <a name="remarks"></a>Remarques

La chaîne de version doit utiliser la version _MajorVersion_. Format _MinorVersion_ (par exemple, 1,4730). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

