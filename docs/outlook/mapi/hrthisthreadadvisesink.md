---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346836"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un récepteur de notification qui encapsule un récepteur de notifications existant pour la sécurité des threads. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Paramètres

 _lpAdviseSink_
  
> dans Pointeur vers le récepteur de notifications à inclure dans un wrapper. 
    
 _lppAdviseSink_
  
> remarquer Pointeur vers un pointeur vers un nouveau récepteur de notification qui encapsule le récepteur de notification pointé par le paramètre _lpAdviseSink_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

L'objectif du wrapper est de s'assurer que la notification est appelée sur le même thread qui a appelé la fonction **HrThisThreadAdviseSink** . Cette fonction est utilisée pour protéger les rappels de notification qui doivent s'exécuter sur un thread particulier. 
  
Les applications clientes doivent utiliser **HrThisThreadAdviseSink** pour limiter la génération des notifications, c'est-à-dire lorsque des appels sont passés à la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) de l'objet de récepteur de notification transmis par le client dans un avis précédent. ** **appel. Si les notifications peuvent être générées de manière arbitraire, une implémentation de notification peut forcer un client à effectuer une opération multithread lorsque cela n'est pas approprié. Par exemple, un client peut utiliser une bibliothèque, telle que l'une des bibliothèques de classes Microsoft Foundation, qui ne prend pas en charge les appels multithread. La notification sur un autre thread rendrait ce client difficile à tester et sujette à des erreurs. 
  
 **HrThisThreadAdviseSink** garantit que les appels **OnNotify** se produisent uniquement aux moments appropriés: 
  
- Lors du traitement d'un appel à n'importe quelle méthode MAPI. 
    
- Lors du traitement des messages Windows. 
    
Lorsque **HrThisThreadAdviseSink** est implémenté, tous les appels à la méthode **OnNotify** du nouveau récepteur de conseils sur n'importe quel thread entraîne l'exécution de la méthode de notification d'origine sur le thread sur lequel **HrThisThreadAdviseSink** a été appelé. 
  
Pour plus d'informations sur les récepteurs de notification et de notification, consultez la rubrique [Event notification in MAPI](event-notification-in-mapi.md) et Implementing a Advise [Sink Object](implementing-an-advise-sink-object.md). 
  

