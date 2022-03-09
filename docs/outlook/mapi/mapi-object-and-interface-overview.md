---
title: Vue d’ensemble de l’interface et de l’objet MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
ms.openlocfilehash: a0dd80619b50420e1cae218451d4e4af9762563b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372520"
---
# <a name="mapi-object-and-interface-overview"></a>Vue d’ensemble de l’interface et de l’objet MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un objet MAPI est une classe d’objet C++ ou une structure de données C héritée d’une ou de plusieurs interfaces MAPI, ou de collections de fonctions connexes. Ces collections de fonctions associées sont connues des développeurs C++ en tant que fonctions virtuelles pures. Pour une fonction virtuelle pure, MAPI fournit uniquement le prototype de fonction, et non une implémentation. Une application cliente, un fournisseur de services ou MAPI doit fournir cette implémentation en créant une classe d’objet qui hérite de l’interface et se conforme aux descriptions de fonction de l’API de messagerie. Une interface MAPI ne peut être ins instantiée que par le biais d’une classe héritée.
  
Il existe de nombreux objets MAPI différents, chaque objet héritant d’une interface qui est finalement héritée de l’interface [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) . **IUnknown est l’interface** de base COM (Component Object Model) OLE. Il fournit aux objets MAPI un mécanisme standard de communication et de contrôle. COM détermine comment les implémenteurs d’objets gèrent les problèmes tels que la gestion de la mémoire, la gestion des paramètres et le multithreading. En respectant ce modèle, un implémenteur d’objet respecte un contrat spécifié par les interfaces incluses dans l’objet. 
  
De nombreuses interfaces MAPI sont héritées directement **d’IUnknown**, tandis que d’autres sont héritées indirectement via l’une des deux autres interfaces de base : [IMAPIProp : IUnknown](imapipropiunknown.md) pour la gestion des propriétés et [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) pour l’accès aux dossiers et aux carnets d’adresses. Les interfaces de base ne sont jamais implémentées en tant qu’objets autonomes distincts ; ils sont toujours implémentés dans le cadre d’autres objets, objets qui implémentent des interfaces dérivées. 
  
MAPI définit de nombreux types d’objets, chacun implémenté par un ou plusieurs composants MAPI. Les objets implémentés par les clients sont utilisés par MAPI, par des fournisseurs de services et par des composants de formulaire personnalisés. Les objets implémentés par les fournisseurs de services sont généralement utilisés par MAPI et par les clients. Les objets implémentés par les fournisseurs de bibliothèques de formulaires et les serveurs de formulaires sont utilisés par d’autres composants de formulaire et par des clients. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Concepts MAPI](mapi-concepts.md)

