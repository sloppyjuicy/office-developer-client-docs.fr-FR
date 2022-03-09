---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
ms.localizationpriority: high
ms.openlocfilehash: 0872c2a8922ee00f8bcc99ecca4679966ffce68e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372149"
---
# <a name="tchar"></a>TCHAR

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Chaîne de caractères Win32 qui peut être utilisée pour décrire les chaînes ANSI, DBCS ou Unicode. Pour les plateformes ANSI et DBCS, TCHAR est défini comme suit :
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>Remarques

Pour les plateformes Unicode, TCHAR est défini comme synonyme du type WCHAR. 
  
Les clients MAPI peuvent utiliser le type de données TCHAR pour représenter une chaîne de type WCHAR ou CHAR. Veillez à bien définir la constante symbolique UNICODE et à limiter la plateforme lorsque cela est nécessaire. MAPI interprète les informations de plateforme et traduit en interne les caractères TCHAR dans la chaîne appropriée. Le type de propriété MAPI, PT_TSTRING, fonctionne comme le type de données TCHAR. Lorsque la plateforme prend en charge le langage Unicode, le type PT_UNICODE est affecté aux propriétés de type PT_TSTRING lors de la compilation. Si la plateforme ne prend pas en charge le langage Unicode, ces propriétés ont le type PT_STRING8.
  
Pour plus d’informations sur cette fonctionnalité, voir [Jeux de caractères](mapi-character-sets.md) et [Liste de types de propriétés](property-types.md). 
  
## <a name="see-also"></a>Voir aussi



[Types de données MAPI](mapi-data-types.md)

