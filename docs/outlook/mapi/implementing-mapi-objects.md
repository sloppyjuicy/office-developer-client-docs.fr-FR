---
title: Implémentation d’objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397099"
---
# <a name="implementing-mapi-objects"></a>Implémentation d’objets MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Objets MAPI peuvent être implémentés à l’aide des classes C++ ou C des structures de données, en fonction du langage et l’API de définie un client ou fournisseur de services. Fournisseurs de services peuvent être écrites en C ou C++ avec l’interface de fournisseur de services MAPI ; les applications clientes peuvent également utiliser C ou C++. Si possible, clients et fournisseurs de services qui utilisent l’interface de programmation orientée objet utilisez C++. 
  
C++ est le meilleur choix car MAPI est une technologie orientée objet et C++ prête plus facilement à un développement orienté objet. Le code qui en résulte est plus simple et plus simple, ce qui facilite la maintenance. La documentation de MAPI s’adresse essentiellement aux développeurs C++ ; toutes les descriptions de syntaxe pour les méthodes d’interface MAPI dans cette référence sont en langage C++.
  
Développeurs peuvent utiliser Microsoft Visual Studio et les outils de développement tiers pour développer des solutions qui appellent MAPI. Notez que les développeurs doivent utiliser C ou C++ non managé, mais non gérés C++ pour écrire des solutions de MAPI.
  
Lorsqu’un objet MAPI est implémenté, un client ou fournisseur de services crée du code pour toutes les méthodes d’interface, le code pour les méthodes privées qui sont spécifiques à l’implémentation et le code pour prendre en charge les données membres privées pour maintenir les informations d’état. Le code pour les méthodes d’interface doit respecter les spécifications publiées par MAPI qui documentent le comportement attendu. 
  
Il existe de nombreuses macros dans le fichier d’en-tête Mapidefs.h et fichiers d’en-tête OLE clients et fournisseurs de services dans une langue peuvent utiliser pour leur permettre de leurs définitions d’objets MAPI. Par exemple, il existe une macro pour définir les méthodes de chaque interface MAPI. La macro pour définir les méthodes de l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) apparaît dans Mapidefs.h comme suit : 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Voir aussi



[Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)

