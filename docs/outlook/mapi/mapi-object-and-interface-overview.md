---
title: Vue d'ensemble de l'objet et de l'interface MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345786"
---
# <a name="mapi-object-and-interface-overview"></a>Vue d'ensemble de l'objet et de l'interface MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un objet MAPI est une classe d'objet C++ ou une structure de données C héritée d'une ou de plusieurs interfaces MAPI, ou des collections de fonctions associées. Ces collections de fonctions connexes sont connues des développeurs C++ comme des fonctions virtuelles pures. Pour une fonction virtuelle pure, MAPI fournit uniquement le prototype de fonction, pas une implémentation. Une application cliente, un fournisseur de services ou MAPI doit fournir cette implémentation en créant une classe d'objet qui hérite de l'interface et conforme aux descriptions de fonction de l'API de messagerie. Une interface MAPI ne peut être instanciée que par le biais d'une classe héritée.
  
Il existe de nombreux objets MAPI différents, chaque objet qui hérite d'une interface qui est finalement héritée de l'interface [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) . **IUnknown** est l'interface de base com (Component Object Model) de OLE. Il fournit des objets MAPI avec un mécanisme standard de communication et de contrôle. COM détermine comment les implémenteurs d'objets gèrent les problèmes tels que la gestion de la mémoire, la gestion des paramètres et le multithreading. En se conformant à ce modèle, un implémenteur d'objet adhère à un contrat tel que spécifié par les interfaces incluses dans l'objet. 
  
De nombreuses interfaces MAPI sont directement héritées de **IUnknown**, tandis que d'autres sont indirectement héritées par le biais de l'une des deux autres interfaces de base: [IMAPIProp: IUnknown](imapipropiunknown.md) pour la gestion des propriétés et [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) pour le dossier et accès au carnet d'adresses. Les interfaces de base ne sont jamais implémentées en tant qu'objets autonomes distincts; elles sont toujours implémentées dans le cadre d'autres objets, objets qui implémentent des interfaces dérivées. 
  
MAPI définit de nombreux types d'objets, chacun étant implémenté par un ou plusieurs composants MAPI. Les objets implémentés par les clients sont utilisés par MAPI, par les fournisseurs de services et par les composants de formulaire personnalisés. Les objets implémentés par les fournisseurs de services sont généralement utilisés par MAPI et par les clients. Les objets implémentés par les fournisseurs de bibliothèques de formulaires et les serveurs de formulaires sont utilisés par les autres composants de formulaire et par les clients. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Concepts MAPI](mapi-concepts.md)

