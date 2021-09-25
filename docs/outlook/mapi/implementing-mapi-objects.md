---
title: Mise en œuvre des objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 64ea298fc078e2848093182bce2bf85f9b3bfc23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584254"
---
# <a name="implementing-mapi-objects"></a>Mise en œuvre des objets MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets MAPI peuvent être implémentés à l’aide de classes C++ ou de structures de données C, en fonction du langage et de l’ensemble d’API utilisé par un client ou un fournisseur de services. Les fournisseurs de services peuvent être écrits en C ou C++ avec l’interface du fournisseur de services MAPI . les applications clientes peuvent également utiliser C ou C++. Si possible, les clients et les fournisseurs de services qui utilisent l’interface de programmation orientée objet doivent utiliser C++. 
  
C++ est le choix préféré, car MAPI est une technologie orientée objet, et C++ se prête plus facilement au développement orienté objet. Le code qui en résulte est plus simple et plus simple, ce qui facilite sa maintenance. La documentation MAPI est écrite principalement pour les développeurs C++. Toutes les descriptions de syntaxe pour les méthodes d’interface MAPI dans cette référence sont en C++.
  
Les développeurs peuvent utiliser Microsoft Visual Studio et des outils de développement tiers pour développer des solutions qui appellent MAPI. Notez que les développeurs doivent utiliser C ou C++ non géré, mais pas C++ géré pour écrire des solutions MAPI.
  
Lorsqu’un objet MAPI est implémenté, un client ou un fournisseur de services crée du code pour toutes les méthodes d’interface, du code pour toutes les méthodes privées spécifiques à l’implémentation et du code pour prendre en charge les membres de données privées pour la maintenance des informations d’état. Le code des méthodes d’interface doit respecter les spécifications publiées par MAPI qui documentent le comportement attendu. 
  
Il existe de nombreuses macros dans le fichier d’en-tête Mapidefs.h et les fichiers d’en-tête OLE que les clients et fournisseurs de services dans les deux langues peuvent utiliser pour les aider avec leurs définitions d’objets MAPI. Par exemple, il existe une macro pour définir les méthodes de chacune des interfaces MAPI. La macro qui définit les méthodes de l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) apparaît dans Mapidefs.h comme suit : 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

