---
title: Utilisation des objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: d732efe5276f4756f43b4aca46e1c33d6f103844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329675"
---
# <a name="using-mapi-objects"></a>Utilisation des objets MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients et les fournisseurs de services utilisent les objets MAPI en appelant les méthodes dans leurs implémentations d'interface. Il s'agit de la seule façon dont les objets MAPI peuvent être utilisés; les méthodes implémentées par un objet en dehors d'une interface MAPI ne sont pas accessibles publiquement. Étant donné que toutes les interfaces d'un objet sont liées par héritage, l'utilisateur d'un objet peut appeler des méthodes dans l'interface de base ou l'une des interfaces héritées comme si elles appartiennent à la même interface. 
  
Lorsque l'utilisateur d'un objet souhaite appeler une méthode et que cet objet implémente plusieurs interfaces liées par héritage, l'utilisateur n'a pas besoin de savoir à quelle interface la méthode appartient. L'utilisateur peut appeler n'importe laquelle des méthodes sur l'une des interfaces à l'aide d'un seul pointeur vers l'objet. Par exemple, l'illustration suivante montre comment une application cliente utilise un objet Folder. Les objets Folder implémentent l'interface [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) , qui hérite indirectement de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) via [IMAPIProp: IUnknown](imapipropiunknown.md) et [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). Un client peut appeler l'une des méthodes **IMAPIProp** , telles que [IMAPIProp:: GetProps](imapiprop-getprops.md), et l'une des méthodes [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) , telles que [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md), de la même manière avec le même pointeur d'objet. Un client ne connaît pas ou n'est pas concerné par le fait que ces appels appartiennent à des interfaces différentes.
  
**Utilisation client d’un objet de dossier**
  
![Utilisation d'un objet Folder par le client] (media/amapi_40.gif "Utilisation d'un objet Folder par le client")
  
Ces appels sont traduits en code différemment selon que le client effectuant les appels est écrit en C ou C++. Avant qu'un appel à une méthode ne puisse être effectué, un pointeur vers l'implémentation de l'interface doit être récupéré. Les pointeurs d'interface peuvent être obtenus des façons suivantes:
  
- Appel d'une méthode sur un autre objet.
    
- Appel d'une fonction API.
    
- Appel de la méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) sur l'objet cible. 
    
MAPI fournit plusieurs méthodes et fonctions d'API qui renvoient des pointeurs vers des implémentations d'interface. Par exemple, les clients peuvent appeler la méthode [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) pour récupérer un pointeur vers un objet table qui fournit l'accès aux informations du fournisseur de banque de messages par le biais de l'interface [IMAPITable: interface IUnknown](imapitableiunknown.md) . Les fournisseurs de services peuvent appeler la fonction [CreateTable](createtable.md) de l'API pour récupérer un pointeur vers un objet de données de tableau. Lorsqu'aucune fonction ni méthode n'est disponible, et que les clients ou les fournisseurs de services ont déjà un pointeur vers un objet, ils peuvent appeler la méthode **QueryInterface** de l'objet pour récupérer un pointeur vers une autre des implémentations d'interface de l'objet. 
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble de l'objet et de l'interface MAPI](mapi-object-and-interface-overview.md)

