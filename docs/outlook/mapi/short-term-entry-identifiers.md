---
title: Identificateurs d’entrée à court terme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f601971e61eb6430bef9d50b093642ee04b14044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787157"
---
# <a name="short-term-entry-identifiers"></a>Identificateurs d’entrée à court terme

**S’applique à**: Outlook 
  
Un identificateur d’entrée à court terme est affecté par un fournisseur de services à un objet lorsque l’identificateur doit être construit rapidement et ne doit pas au dernier sur heure ou à distance. Le caractère unique d’un identificateur d’entrée à court terme est garanti uniquement pendant la durée de la session en cours sur la station de travail en cours. En règle générale, un identificateur d’entrée à court terme est valide uniquement jusqu'à ce que l’objet qu’il représente. 
  
Identificateurs d’entrée à court terme sont affectés aux lignes dans les tableaux et aux entrées de boîtes de dialogue, où il est nécessaire de fournir rapidement des données pour la navigation. Par exemple, les fournisseurs de magasins de message affecter à court terme identificateurs d’entrée aux lignes des messages dans une table des matières et aux destinataires dans un tableau de destinataires. 

Clients peuvent utiliser ces identificateurs d’entrée à court terme pour ouvrir les objets représentés par les lignes de tableau. Toutefois, contrairement aux identificateurs d’entrée à long terme qui peuvent être utilisés avec l’une des méthodes **OpenEntry** , identificateurs d’entrée à court terme doivent être utilisés avec la méthode de **OpenEntry** du conteneur. 
  
## <a name="implementing-short-term-entry-identifiers"></a>L’implémentation d’identificateurs d’entrée à court terme

Les méthodes les plus courantes pour implémenter les identificateurs d’entrée à court terme sont les suivantes :
  
- Fabrication les identificateurs d’entrée à court terme comme les identificateurs à long terme, en laissant tous les indicateurs non définie. 
    
- Rendre les identificateurs d’entrée à court terme diffère les identificateurs à long terme, la définition de tous les indicateurs. 
    
Les clients peuvent identifier un identificateur d’entrée à court terme du second type en examinant son membre **abFlags** comme suit : 
  
```cpp
abFlags[0] = 0xFF;
 
```

Certains fournisseurs de services désactivez un ou plusieurs indicateurs pour créer des identificateurs d’entrée à court terme dont la validité supérieure. Par exemple, les membres **abFlags** suivants représentent les identificateurs d’entrée à court terme qui peuvent être utilisés pour plusieurs jours ou plusieurs sessions : 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Clients rapidement acquièrent, utilisent et ignorer les identificateurs d’entrée à court terme. Pour l’essentiel, ils peuvent être utilisés dans la même manière que les identificateurs d’entrée à long terme. Il peuvent être récupérés à partir d’une table, transmises à la méthode **OpenEntry** , par rapport à la méthode **CompareEntryIDs** . La seule exception est qu’ils ne sont jamais retournés par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . Les propriétés renvoyées à partir de **GetProps** sont toujours des identificateurs d’entrée à long terme. 
  
## <a name="see-also"></a>Voir aussi

- [Identificateurs d’entrée MAPI](mapi-entry-identifiers.md)

