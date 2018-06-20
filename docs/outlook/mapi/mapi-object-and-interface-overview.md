---
title: Objet MAPI et vue d’ensemble de l’Interface
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8882457ff99f4150f2c9b086b92af32de29d60a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784641"
---
# <a name="mapi-object-and-interface-overview"></a>Objet MAPI et vue d’ensemble de l’Interface

  
  
**S’applique à**: Outlook 
  
Un objet MAPI est une classe d’objet C++ ou d’une structure de données C hérité d’une ou plusieurs des interfaces MAPI ou des collections de fonctions connexes. Ces collections de fonctions connexes sont appelées pour les développeurs C++ fonctions virtuelles pures. Pour une fonction virtuelle pure, MAPI fournit uniquement le prototype de fonction, pas une implémentation. Il est prévu qu’une application cliente, un fournisseur de services ou MAPI fournira cette implémentation en créant un objet de classe qui hérite de l’interface et est conforme à la description de la fonction de l’API de messagerie. Une interface MAPI peut être instanciée uniquement par le biais d’une classe héritée.
  
Il existe de nombreux objets MAPI différents, chaque objet qui hérite d’une interface qui est finalement héritée de l’interface [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) . **IUnknown** est l’interface de base OLE composant COM (Object Model). Il fournit des objets MAPI avec un mécanisme standard de communication et de contrôle. COM détermine comment gérer les problèmes de gestion de la mémoire, gestion de paramètre, l’implémentation d’objet et le multithreading. En répondant à ce modèle, une implémentation de l’objet est conforme à un contrat tel que spécifié par les interfaces inclus dans l’objet. 
  
Nombre d’interfaces MAPI est héritée directement à partir **IUnknown**, tandis que d’autres personnes sont héritées indirectement par le biais d’une des deux autres interfaces de base : [IMAPIProp : IUnknown](imapipropiunknown.md) pour la gestion de la propriété et [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) pour le dossier et accès au carnet d’adresses. Interfaces de base ne sont jamais implémentées comme distinct, objets autonomes ; ils sont toujours exécutées dans le cadre d’autres objets, les objets qui implémentent les interfaces dérivées. 
  
MAPI définit de nombreux types d’objets, chacun implémenté par un ou plusieurs composants MAPI. Objets implémentés par les clients qui sont utilisés par MAPI, les fournisseurs de services et par les composants de formulaire personnalisé. Objets implémentés par les fournisseurs de services sont généralement utilisés par MAPI et par les clients. Objets implémentés par les fournisseurs de bibliothèques de formulaires et les serveurs de formulaire sont utilisés par d’autres composants de formulaire et par les clients. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Concepts MAPI (en anglais)](mapi-concepts.md)

