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
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Renvoie une chaîne qui représente le numéro de version du fournisseur de ce réseau social. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Valeur de propriété

Chaîne qui contient le numéro de version du fournisseur.
  
## <a name="remarks"></a>Remarques

La chaîne de version doit utiliser le _MajorVersion_. Format _MinorVersion_ (par exemple, 1.4730). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

