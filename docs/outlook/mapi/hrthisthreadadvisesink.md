---
title: HrThisThreadAdviseSink
description: Cet article décrit la fonction HrThisThreadAdviseSink et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
ms.openlocfilehash: f4298a5da5ecd0f3844e3fac9848d4424c2638bd
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816408"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un récepteur de conseils qui encapsule un récepteur de conseils existant pour la sécurité des threads. 
  
|Propriété |Valeur |
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
  
> [in] Pointeur vers le récepteur de conseil à encapsulier. 
    
 _lppAdviseSink_
  
> [out] Pointeur vers un pointeur vers un nouveau récepteur de conseils qui encapsule le récepteur conseiller pointé par le paramètre  _lpAdviseSink_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

L’objectif du wrapper est de s’assurer que la notification est appelée sur le même thread que la fonction **HrThisThreadAdviseSink** . Cette fonction est utilisée pour protéger les rappels de notification qui doivent s’exécuter sur un thread particulier. 
  
Les applications clientes doivent utiliser **HrThisThreadAdviseSink** pour limiter le moment où des notifications sont générées, c’est-à-dire lorsque des appels sont effectués à la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de l’objet récepteur conseiller passé par le client lors d’un appel **Conseiller** précédent. Si les notifications sont autorisées à être générées arbitrairement, une implémentation de notification peut forcer un client à effectuer une opération multithread lorsque cela ne serait pas approprié. Par exemple, un client peut utiliser une bibliothèque, telle que l’une des bibliothèques de classes Microsoft Foundation, qui ne prend pas en charge les appels multithread. La notification sur un autre thread rendrait ce client difficile à tester et susceptible d’être erroné. 
  
 **HrThisThreadAdviseSink** s’assure que les appels **OnNotify** se produisent uniquement aux moments appropriés : 
  
- Pendant le traitement d’un appel à une méthode MAPI. 
    
- Pendant le traitement des messages Windows. 
    
Lorsque **HrThisThreadAdviseSink** est implémenté, tout appel à la méthode **OnNotify** du nouveau récepteur de conseils sur un thread entraîne l’exécution de la méthode de notification d’origine sur le thread sur lequel **HrThisThreadAdviseSink** a été appelé. 
  
Pour plus d’informations sur les récepteurs de notification et de conseil, consultez [Notification d’événement dans MAPI](event-notification-in-mapi.md) et [Implémentation d’un objet récepteur De conseils](implementing-an-advise-sink-object.md). 
  

