---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 59f3034fa4217f3ee43cda959e07fd0bc9f8f784
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551645"
---
# <a name="exchange_store_version_num"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Stocke les informations de version des Microsoft Exchange Server à qui les comptes d’un Microsoft Office Outlook sont connectés.
  
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
  
- Numéro de version principal généralement incrémenté lorsqu’une version contient d’importantes nouvelles fonctionnalités et modifications de fonctionnalités.
    
 _wMinorVersion_
  
- Numéro de version mineure qui correspond à un numéro de version majeur spécifique et qui est généralement incrémenté lorsqu’une version contient de nouvelles fonctionnalités mineures ou des correctifs significatifs.
    
 _wBuild_
  
- Numéro de build principal qui correspond à des numéros de version principaux et mineurs spécifiques et qui est généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou correctifs. Cette valeur est également incrémentée lorsque la publication est une branche de code interne majeure ou un jalon, tel qu’un candidat à la publication.
    
 _wMinorBuild_
  
- Numéro de build mineure généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou correctifs correspondant à une build majeure spécifique qui indique une branche de code majeure ou un jalon.
    
## <a name="see-also"></a>Voir aussi



[À propos des ajouts MAPI](about-mapi-additions.md)
  
[Propriété canonique PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

