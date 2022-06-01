---
title: DISMISSMODELESS
description: DISMISSMODELESS définit une fonction de rappel que MAPI appelle lorsqu’il a ignoré une boîte de dialogue de carnet d’adresses sans mode.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
ms.openlocfilehash: 64d19c65b5c9401e080f721d13f3e54e56044223
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811794"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

**S’applique à** : Outlook 2013 | Outlook 2016
  
Définit une fonction de rappel que MAPI appelle lorsqu’elle a ignoré une boîte de dialogue de carnet d’adresses sans mode.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Fonction définie implémentée par :  <br/> |Applications clientes  <br/> |
|Fonction définie appelée par :  <br/> |MAPI  <br/> |

```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Valeur spécifique à l’implémentation généralement utilisée pour transmettre des informations d’interface utilisateur à une fonction. Par exemple, dans Microsoft Windows ce paramètre est le handle de fenêtre parent de la boîte de dialogue et est de type HWND, converti en **ULONG_PTR**. La valeur zéro indique qu’il n’y a pas de fenêtre parente.

 _lpvContext_
  
> [in] Pointeur vers une valeur arbitraire transmise à la fonction de rappel lorsque MAPI l’appelle. Cette valeur peut représenter une adresse d’importance pour l’application cliente. En règle générale, pour le code C++, _lpvContext_ est un pointeur vers l’adresse d’une instance d’objet C++.

## <a name="return-value"></a>Valeur renvoyée

Aucun
  
## <a name="remarks"></a>Remarques

Lorsque l’application cliente appelle une boîte de dialogue carnet d’adresses sans mode, elle inclut dans sa boucle de message Windows un appel à une fonction basée sur le prototype [ACCELERATEABSDI](accelerateabsdi.md), qui recherche et traite les touches d’accélérateur. Lorsque la boîte de dialogue est fermée, MAPI appelle la fonction **DISMISSMODELESS** afin que l’application cliente cesse d’appeler la fonction **ACCELERATEABSDI** .
  
## <a name="see-also"></a>Voir aussi

[ADRPARM](adrparm.md)
