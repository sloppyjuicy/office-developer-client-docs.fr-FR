---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
ms.openlocfilehash: b164f9c0ccd3ad242d827d0e66ca24e57aa35dd5
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381802"
---
# <a name="exchange_store_version_num"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Stocke les informations de version pour les Microsoft Exchange Server comptes dans un profil Microsoft Office Outlook sont connectés.
  
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
  
- Numéro de build principal qui correspond à des numéros de version principaux et mineurs spécifiques et qui est généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou correctifs. Cette valeur est également incrémentée lorsque la publication est une branche ou un jalon majeur du code interne, tel qu’un candidat à la publication.
    
 _wMinorBuild_
  
- Numéro de build mineure généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou correctifs correspondant à une build majeure spécifique qui indique une branche de code majeure ou un jalon.
    
## <a name="see-also"></a>Voir aussi



[À propos des ajouts MAPI](about-mapi-additions.md)
  
[Propriété canonique PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

