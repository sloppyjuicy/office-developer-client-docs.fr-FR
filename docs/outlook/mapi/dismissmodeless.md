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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c66ff2338eb5751dbffe392a6a26258fb1c89476
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565836"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel appels MAPI lorsqu’il a rejeté une boîte de dialogue non modale adresse téléchargeable. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Fonction implémentée par :  <br/> |Applications clientes  <br/> |
|Fonction appelée par :  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Une valeur spécifique à l’implémentation est généralement utilisée pour transmettre des informations d’interface utilisateur à une fonction. Par exemple, dans Microsoft Windows ce paramètre est le handle de fenêtre parent pour la boîte de dialogue et est de type HWND, d’une **ULONG_PTR entière**. La valeur zéro indique aucune fenêtre parent est. 
    
 _lpvContext_
  
> [in] Pointeur vers une valeur arbitraire transmis à la fonction de rappel lorsque MAPI il l’appelle. Cette valeur peut représenter une adresse de l’argument précision à l’application cliente. En règle générale, pour le code C++, _lpvContext_ est un pointeur vers l’adresse d’une instance d’objet C++. 
    
## <a name="return-value"></a>Valeur renvoy�e

Aucune
  
## <a name="remarks"></a>Remarques

Lorsque l’application cliente appelle une boîte de dialogue non modale adresse téléchargeable, il inclut dans sa boucle de message Windows un appel à une fonction basée sur le prototype [ACCELERATEABSDI](accelerateabsdi.md) , qui recherche et traite les touches de raccourci. Lorsque la boîte de dialogue est fermée, les appels MAPI que fonction en fonction de la **DISMISSMODELESS** afin que l’application cliente s’arrête **ACCELERATEABSDI** l’appel en fonction de fonction. 
  
## <a name="see-also"></a>Voir aussi



[ADRPARM](adrparm.md)

