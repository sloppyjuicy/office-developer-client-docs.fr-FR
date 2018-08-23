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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3df5e012867623d1c5e8fb5c3c93103548ab97be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588383"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée un récepteur de notifications qui encapsule un récepteur de notifications existant pour la sécurité des threads. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Paramètres

 _lpAdviseSink_
  
> [in] Pointeur vers le récepteur de notifications à encapsuler. 
    
 _lppAdviseSink_
  
> [out] Pointeur vers un pointeur vers un nouveau récepteur de notifications qui encapsule le récepteur de notifications indiqué par le paramètre _lpAdviseSink_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

L’objectif du wrapper est pour vous assurer que la notification est appelée sur le même thread qui a appelé la fonction **HrThisThreadAdviseSink** . Cette fonction est utilisée pour protéger les rappels de notification qui doivent s’exécuter sur un thread particulier. 
  
Applications clientes permet de limiter les notifications sont générées, autrement dit, lors des appels à la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de l’objet de récepteur advise transmis par le client dans une précédente **Advise **HrThisThreadAdviseSink** **d’appel. Si les notifications sont autorisées à générer arbitrairement, une implémentation de notification peut forcer un client dans opération multithread lorsque qui ne serait pas appropriée. Par exemple, un client peut utiliser une bibliothèque, telle qu’une des bibliothèques de classes Microsoft Foundation, qui ne prend pas en charge les appels multithreads. Notification sur un autre thread qu’un tel client difficile à tester et source d’erreurs. 
  
 **HrThisThreadAdviseSink** permet de s’assurer que les appels **OnNotify** se produisent uniquement à ces heures appropriés : 
  
- Lors du traitement d’un appel à n’importe quelle méthode MAPI. 
    
- Lors du traitement des messages Windows. 
    
Lorsque **HrThisThreadAdviseSink** est implémentée, les appels à **OnNotify** (méthode) du nouveau récepteur advise sur n’importe quel thread entraînent la méthode de notification d’origine à exécuter sur le thread sur lequel **HrThisThreadAdviseSink** a été appelée. 
  
Pour plus d’informations sur la notification et les récepteurs de notifications, voir [Notification d’événement MAPI](event-notification-in-mapi.md) et [l’implémentation d’un objet récepteur de notification](implementing-an-advise-sink-object.md). 
  

