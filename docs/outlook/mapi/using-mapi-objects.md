---
title: Utilisation d’objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a355faf85a44f6257b77b7171aa965faabf57fe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787456"
---
# <a name="using-mapi-objects"></a>Utilisation d’objets MAPI

**S’applique à**: Outlook 
  
Clients et fournisseurs de services utilisent MAPI d’objets en appelant les méthodes dans leurs implémentations d’interface. Il s’agit de la seule façon que les objets MAPI peuvent être utilisés ; méthodes qui sont implémentées par un objet en dehors d’une interface MAPI ne sont pas accessibles au public. Étant donné que toutes les interfaces d’un objet sont liées par le biais de l’héritage des autorisations, utilisateur d’un objet peut appeler des méthodes dans l’interface de base ou un des interfaces héritées comme s’ils appartiennent à la même interface. 
  
Lorsque l’utilisateur d’un objet souhaite émettre un appel à une méthode et cet objet implémente plusieurs interfaces liées par le biais de l’héritage des autorisations, l’utilisateur ne doit pas savoir interface à laquelle appartient la méthode. L’utilisateur peut appeler une des méthodes sur n’importe lequel des interfaces avec un pointeur vers l’objet unique. Par exemple, l’illustration suivante montre comment une application cliente utilise un objet folder. Implémentent des objets de dossier la [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface qui hérite [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indirectement via [IMAPIProp : IUnknown](imapipropiunknown.md) et [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). Un client peut appeler une des méthodes **IMAPIProp** , tel [IMAPIProp::GetProps](imapiprop-getprops.md)et l’autre de la [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) méthodes, telles [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), de la même façon avec le pointeur d’objet. Un client n’est pas connaissance ou affectés par le fait que ces appels appartiennent à différentes interfaces.
  
**Utilisation d’un objet folder**
  
![Utiliser des clients d’un objet folder] (media/amapi_40.gif "Utiliser des clients d’un objet folder")
  
Ces appels traduisent le code différemment selon que le client de l’appel est écrit en C ou C++. Avant d’effectuer un appel à une méthode, un pointeur vers l’implémentation d’interface doit être récupéré. Pointeurs d’interface peuvent être obtenus de la manière suivante :
  
- Appelez une méthode sur un autre objet.
    
- Appel d’une fonction d’API.
    
- L’appel de la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) sur l’objet cible. 
    
MAPI fournit plusieurs méthodes et fonctions de l’API qui retournent des pointeurs vers des implémentations d’interface. Par exemple, les clients peuvent appeler la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour récupérer un pointeur vers un objet table qui fournit l’accès aux informations de fournisseur de magasin de message par le biais de la [IMAPITable : IUnknown](imapitableiunknown.md) interface. Fournisseurs de services peuvent appeler la fonction API [Create table](createtable.md) pour récupérer un pointeur vers un objet de données de table. Lorsqu’il n’y a aucune fonction ou une méthode disponibles et les clients ou fournisseurs de services disposez déjà d’un pointeur vers un objet, elles peuvent appeler la méthode **QueryInterface** de l’objet pour extraire un pointeur vers un autre des implémentations d’interface de l’objet. 
  
## <a name="see-also"></a>Voir aussi

- [Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)

