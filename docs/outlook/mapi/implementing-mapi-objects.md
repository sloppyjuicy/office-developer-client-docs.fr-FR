---
title: Implémentation d'objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310170"
---
# <a name="implementing-mapi-objects"></a>Implémentation d'objets MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets MAPI peuvent être implémentés à l'aide de classes C++ ou de structures de données C, selon le langage et l'ensemble d'API que le client ou le fournisseur de services utilise. Les fournisseurs de services peuvent être écrits en C ou C++ avec l'interface du fournisseur de services MAPI; les applications clientes peuvent également utiliser C ou C++. Dans la mesure du possible, les clients et fournisseurs de services qui utilisent l'interface de programmation orientée objet doivent utiliser C++. 
  
C++ est le choix préféré car MAPI est une technologie orientée objet, et C++ se prête lui-même plus facilement au développement orienté objet. Le code résultant est plus simple et plus simple, ce qui le rend plus facile à gérer. La documentation MAPI est conçue principalement pour les développeurs C++; toutes les descriptions de syntaxe pour les méthodes d'interface MAPI de cette référence sont en C++.
  
Les développeurs peuvent utiliser Microsoft Visual Studio et des outils de développement tiers pour développer des solutions qui appellent MAPI. Notez que les développeurs doivent utiliser C ou le C++ non managé, mais pas C++ pour écrire des solutions MAPI.
  
Lorsqu'un objet MAPI est implémenté, un client ou un fournisseur de services crée du code pour toutes les méthodes d'interface, du code pour toutes les méthodes privées qui sont spécifiques à l'implémentation et du code pour prendre en charge les membres de données privés pour la gestion des informations d'État. Le code des méthodes d'interface doit respecter les spécifications publiées par MAPI pour documenter le comportement attendu. 
  
Il existe de nombreuses macros dans le fichier d'en-tête Mapidefs. h et des fichiers d'en-tête OLE que les clients et les fournisseurs de services dans les deux langages peuvent utiliser pour les aider avec leurs définitions d'objets MAPI. Par exemple, il existe une macro permettant de définir les méthodes de chacune des interfaces MAPI. La macro permettant de définir les méthodes de l'interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) apparaît dans Mapidefs. h de la manière suivante: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Voir aussi



[Vue d'ensemble de l'objet et de l'interface MAPI](mapi-object-and-interface-overview.md)

