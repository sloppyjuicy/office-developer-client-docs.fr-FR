---
title: Identificateurs d’entrée à court terme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339192"
---
# <a name="short-term-entry-identifiers"></a>Identificateurs d’entrée à court terme

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un identificateur d'entrée à court terme est affecté par un fournisseur de services à un objet lorsque ce dernier doit être construit rapidement et n'a pas besoin de la dernière fois ou de la distance. L'unicité d'un identificateur d'entrée à court terme n'est garantie que pendant la durée de vie de la session en cours sur le poste de travail actuel. En règle générale, un identificateur d'entrée à court terme est valide uniquement jusqu'à ce que l'objet qu'elle représente soit libéré. 
  
Les identificateurs d'entrée à court terme sont affectés aux lignes des tableaux et aux entrées dans les boîtes de dialogue, où il est nécessaire de fournir des données rapides pour la navigation. Par exemple, les fournisseurs de banque de messages affectent des identificateurs d'entrée à court terme à des lignes de messages dans une table de contenu et à des destinataires dans une table de destinataires. 

Les clients peuvent utiliser ces identificateurs d'entrée à court terme pour ouvrir les objets représentés par les lignes du tableau. Toutefois, à la différence des identificateurs d'entrée à long terme pouvant être utilisés avec l'une des méthodes **OpenEntry** , les identificateurs d'entrée à court terme doivent être utilisés avec la méthode **OpenEntry** du conteneur. 
  
## <a name="implementing-short-term-entry-identifiers"></a>Implémentation d'identificateurs d'entrée à court terme

Les méthodes les plus courantes pour implémenter des identificateurs d'entrée à court terme sont les suivantes:
  
- Rendre les identificateurs d'entrée à court terme identiques aux identificateurs à long terme, en laissant tous les indicateurs non définis. 
    
- Définition des identificateurs d'entrée à court terme différemment des identificateurs à long terme, définition de tous les indicateurs. 
    
Les clients peuvent identifier un identificateur d'entrée à court terme du deuxième type en examinant son membre **abFlags** comme suit: 
  
```cpp
abFlags[0] = 0xFF;
 
```

Certains fournisseurs de services effacent un ou plusieurs indicateurs pour créer des identificateurs d'entrée à court terme qui ont une plus grande validité. Par exemple, les membres **abFlags** suivants représentent des identificateurs d'entrée à court terme pouvant être utilisés pour plusieurs jours ou plusieurs sessions: 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Les clients acquièrent, utilisent et éliminent rapidement les identificateurs d'entrée à court terme. La plupart du temps, ils peuvent être utilisés de la même manière que les identificateurs d'entrée à long terme. Elles peuvent être récupérées à partir d'une table, transmises à la méthode **OpenEntry** et comparées à la méthode **CompareEntryIDs** . La seule exception est qu'ils ne sont jamais renvoyés à partir de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) . Les propriétés renvoyées par **GetProps** sont toujours des identificateurs d'entrée à long terme. 
  
## <a name="see-also"></a>Voir aussi

- [Identificateurs d'entrée MAPI](mapi-entry-identifiers.md)

