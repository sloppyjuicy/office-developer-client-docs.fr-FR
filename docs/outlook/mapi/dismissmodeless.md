---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428185"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel que MAPI appelle lorsqu’elle a rejeté une boîte de dialogue de carnet d’adresses non modique. 
  
|||
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
  
> [in] Valeur spécifique à l’implémentation généralement utilisée pour transmettre des informations d’interface utilisateur à une fonction. Par exemple, dans Microsoft Windows, ce paramètre est le handle de fenêtre parent de la boîte de dialogue et est de type HWND, cast en **ULONG_PTR**. La valeur zéro indique qu’il n’y a pas de fenêtre parente. 
    
 _lpvContext_
  
> [in] Pointeur vers une valeur arbitraire transmise à la fonction de rappel lorsque MAPI l’appelle. Cette valeur peut représenter une adresse significative pour l’application cliente. En règle générale, pour le code C++,  _lpvContext_ est un pointeur vers l’adresse d’une instance d’objet C++. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun
  
## <a name="remarks"></a>Remarques

Lorsque l’application cliente appelle une boîte de dialogue de carnet d’adresses sans mode, elle inclut dans sa boucle de message Windows un appel à une fonction basée sur le prototype [ACCELERATEABSDI,](accelerateabsdi.md) qui vérifie et traite les touches d’accès rapide. Lorsque la boîte de dialogue est fermée, MAPI appelle la fonction **basée DISMISSMODELESS** afin que l’application cliente cesse d’appeler la fonction **basée sur ACCELERATEABSDI.** 
  
## <a name="see-also"></a>Voir aussi



[ADRPARM](adrparm.md)

