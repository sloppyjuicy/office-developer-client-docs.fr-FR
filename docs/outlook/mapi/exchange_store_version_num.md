---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287034"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Stocke les informations relatives à la version du serveur Microsoft Exchange que les comptes dans un profil Microsoft Office Outlook sont connectés à.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Membres

 _wMajorVersion_
  
- Numéro de version majeure généralement incrémenté lorsqu'une publication contient de nouvelles fonctionnalités et des modifications de fonctionnalité importantes.
    
 _wMinorVersion_
  
- Numéro de version mineure correspondant à un numéro de version principal spécifique et généralement incrémenté lorsqu'une publication contient de nouvelles fonctionnalités mineures ou des correctifs importants.
    
 _wBuild_
  
- Numéro de build majeur correspondant à des numéros de version principaux et mineurs spécifiques, généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou des correctifs. Cette valeur est également incrémentée lorsque la version est une branche de code interne majeure ou une étape majeure, telle qu'une version Release candidate.
    
 _wMinorBuild_
  
- Numéro de version mineure généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou des correctifs correspondant à une build majeure spécifique qui désigne une branche ou un jalon de code principal.
    
## <a name="see-also"></a>Voir aussi



[À propos des ajouts MAPI](about-mapi-additions.md)
  
[Propriété canonique PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

