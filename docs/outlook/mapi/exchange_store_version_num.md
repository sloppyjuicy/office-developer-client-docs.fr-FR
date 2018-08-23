---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594473"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Stocke les informations de version de Microsoft Exchange Server dans un profil de Microsoft Office Outlook, les comptes connectés à.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Members

 _wMajorVersion_
  
- Numéro de version principal est généralement incrémenté lorsqu’une version contient importantes nouvelles fonctionnalités et modifications de fonctionnalités.
    
 _wMinorVersion_
  
- Numéro de version secondaire qui correspond à un numéro de version majeure et qui est généralement incrémenté lorsqu’une version contient les nouvelles fonctionnalités secondaires ou correctifs importants.
    
 _wBuild_
  
- Numéro de version majeur qui correspond aux numéros de version principale et secondaire spécifique et qui est généralement incrémentée dans une version interne qui contient des correctifs ou des nouvelles fonctionnalités. Cette valeur est également incrémentée à la version est une branche de code interne principale ou un jalon, par exemple une version release candidate.
    
 _wMinorBuild_
  
- Numéro de version secondaire est incrémentée généralement dans une version interne qui contient les nouvelles fonctionnalités ou corrige correspondant à une version principale spécifique qui indique une branche de code principal ou un jalon.
    
## <a name="see-also"></a>Voir aussi



[À propos des ajouts MAPI](about-mapi-additions.md)
  
[Propriété canonique PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

