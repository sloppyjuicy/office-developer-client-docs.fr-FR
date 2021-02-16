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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427726"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un sink de conseil qui encapsule un sink de conseil existant pour la sécurité des threads. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Pointeur vers le sink de conseil à wrapped. 
    
 _lppAdviseSink_
  
> [out] Pointeur vers un pointeur vers un nouveau sink de conseil qui encapsule le sink de conseil pointé vers le _paramètre lpAdviseSink._ 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

L’objectif du wrapper est de s’assurer que la notification est appelée sur le même thread que celui qui a appelé la fonction **HrThisThreadAdviseSink.** Cette fonction est utilisée pour protéger les rappels de notification qui doivent s’exécuter sur un thread particulier. 
  
Les applications clientes doivent utiliser **HrThisThreadAdviseSink** pour limiter le moment où des notifications sont générées, c’est-à-dire lorsque des appels sont  effectués à la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de l’objet de réception de notification transmis par le client dans un appel de notification précédent. Si les notifications sont autorisées à être générées arbitrairement, une implémentation de notification peut forcer un client à une opération multithread alors que cela ne serait pas approprié. Par exemple, un client peut utiliser une bibliothèque, telle que l’une des bibliothèques de classes Microsoft Foundation, qui ne prend pas en charge les appels multithread. Une notification sur un autre thread rendrait un tel client difficile à tester et sujette à des erreurs. 
  
 **HrThisThreadAdviseSink** s’assure que les appels **OnNotify** se produisent uniquement aux moments appropriés : 
  
- Pendant le traitement d’un appel à n’importe quelle méthode MAPI. 
    
- Pendant le traitement des messages Windows. 
    
Lorsque **HrThisThreadAdviseSink** est implémenté, tout appel à la méthode **OnNotify** du nouveau sink de notification sur n’importe quel thread entraîne l’exécution de la méthode de notification d’origine sur le thread sur lequel **HrThisThreadAdviseSink** a été appelé. 
  
Pour plus d’informations sur les réceptions de notification et de notification, voir notification d’événement dans [MAPI](event-notification-in-mapi.md) et mise en œuvre [d’un objet de réception de conseil.](implementing-an-advise-sink-object.md) 
  

