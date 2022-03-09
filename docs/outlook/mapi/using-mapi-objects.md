---
title: Utilisation des objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
ms.openlocfilehash: 39ec167f32f07e5b19613bf99173f57aeda2fd99
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369538"
---
# <a name="using-mapi-objects"></a>Utilisation des objets MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients et les fournisseurs de services utilisent des objets MAPI en appelant les méthodes dans leurs implémentations d’interface. C’est la seule façon d’utiliser des objets MAPI . implémentées par un objet en dehors d’une interface MAPI ne sont pas accessibles au public. Étant donné que toutes les interfaces d’un objet sont liées par héritage, l’utilisateur d’un objet peut appeler des méthodes dans l’interface de base ou dans l’une des interfaces héritées comme s’ils appartiennent à la même interface. 
  
Lorsque l’utilisateur d’un objet souhaite effectuer un appel à une méthode et que cet objet implémente plusieurs interfaces liées par héritage, l’utilisateur n’a pas besoin de savoir à quelle interface appartient la méthode. L’utilisateur peut appeler n’importe quelle méthode sur n’importe quelle interface avec un pointeur unique vers l’objet. Par exemple, l’illustration suivante montre comment une application cliente utilise un objet dossier. Les objets Folder implémentent l’interface [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) , qui hérite indirectement [d’IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) via [IMAPIProp : IUnknown](imapipropiunknown.md) et [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). Un client peut appeler l’une des méthodes **IMAPIProp** , telles que [IMAPIProp::GetProps](imapiprop-getprops.md), et l’une des méthodes [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) , telles que [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), de la même manière avec le même pointeur d’objet. Un client ne connaît pas ou n’est pas affecté par le fait que ces appels appartiennent à différentes interfaces.
  
**Utilisation client d’un objet de dossier**
  
![Utilisation client d’un objet de dossier](media/amapi_40.gif "Utilisation client d’un objet de dossier")
  
Ces appels se traduisent en code différemment selon que le client qui passe les appels est écrit en C ou C++. Avant de pouvoir appeler une méthode, un pointeur vers l’implémentation de l’interface doit être récupéré. Les pointeurs d’interface peuvent être obtenus des manières suivantes :
  
- Appel d’une méthode sur un autre objet.
    
- Appel d’une fonction API.
    
- Appel de [la méthode IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) sur l’objet cible. 
    
MAPI fournit plusieurs méthodes et fonctions API qui retournent des pointeurs vers des implémentations d’interface. Par exemple, les clients peuvent appeler la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour récupérer un pointeur vers un objet table qui donne accès aux informations du fournisseur de la boutique de messages via l’interface [IMAPITable : IUnknown](imapitableiunknown.md) . Les fournisseurs de services peuvent appeler la fonction API [CreateTable](createtable.md) pour récupérer un pointeur vers un objet de données de table. Lorsqu’aucune fonction ou méthode n’est disponible et que les clients ou fournisseurs de services disposent déjà d’un pointeur vers un objet, ils peuvent appeler la méthode **QueryInterface** de l’objet pour récupérer un pointeur vers une autre implémentation d’interface de l’objet. 
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

