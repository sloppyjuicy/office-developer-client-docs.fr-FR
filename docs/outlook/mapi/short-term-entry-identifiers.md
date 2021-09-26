---
title: Identificateurs d’entrée à court terme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 29dcc79d644ba4a5bf46f06bd8c6466e854ac890
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598982"
---
# <a name="short-term-entry-identifiers"></a>Identificateurs d’entrée à court terme

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un identificateur d’entrée à court terme est attribué par un fournisseur de services à un objet lorsque l’identificateur doit être construit rapidement et n’a pas besoin de durer au fil du temps ou de la distance. L’unicité d’un identificateur d’entrée à court terme est garantie uniquement pendant toute la durée de vie de la session active sur la station de travail actuelle. En règle générale, un identificateur d’entrée à court terme n’est valide que jusqu’à ce que l’objet qu’il représente soit libéré. 
  
Les identificateurs d’entrée à court terme sont affectés aux lignes des tableaux et aux entrées des boîtes de dialogue, où il est nécessaire de fournir rapidement des données pour la navigation. Par exemple, les fournisseurs de magasins de messages affectent des identificateurs d’entrée à court terme à des lignes de messages dans une table des matières et à des destinataires dans une table des destinataires. 

Les clients peuvent utiliser ces identificateurs d’entrée à court terme pour ouvrir les objets représentés par les lignes du tableau. Toutefois, contrairement aux identificateurs d’entrée à long terme qui peuvent être utilisés avec n’importe quelle méthode **OpenEntry,** les identificateurs d’entrée à court terme doivent être utilisés avec la méthode **OpenEntry** du conteneur. 
  
## <a name="implementing-short-term-entry-identifiers"></a>Mise en œuvre d’identificateurs d’entrée à court terme

Les méthodes les plus courantes pour implémenter des identificateurs d’entrée à court terme sont les suivantes :
  
- Rendre les identificateurs d’entrée à court terme identiques aux identificateurs à long terme, en laissant tous les indicateurs non jeu. 
    
- Rendre les identificateurs d’entrée à court terme différents des identificateurs à long terme et définir tous les indicateurs. 
    
Les clients peuvent identifier un identificateur d’entrée à court terme du deuxième type en examinant son membre **abFlags** comme suit : 
  
```cpp
abFlags[0] = 0xFF;
 
```

Certains fournisseurs de services clear one or more flags to create short-term entry identifiers that have greater validity. Par exemple, les membres **abFlags suivants** représentent des identificateurs d’entrée à court terme qui peuvent être utilisés pendant plusieurs jours ou pour plusieurs sessions : 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Les clients achètent, utilisent et rejettent rapidement les identificateurs d’entrée à court terme. En grande partie, ils peuvent être utilisés de la même manière que les identificateurs d’entrée à long terme. Elles peuvent être récupérées à partir d’une table, transmises à la méthode **OpenEntry** et comparées à la méthode **CompareEntryIDs.** La seule exception est qu’elles ne sont jamais renvoyées à partir de la [méthode IMAPIProp::GetProps.](imapiprop-getprops.md) Les propriétés renvoyées par **GetProps** sont toujours des identificateurs d’entrée à long terme. 
  
## <a name="see-also"></a>Voir aussi

- [Identificateurs d’entrée MAPI](mapi-entry-identifiers.md)

