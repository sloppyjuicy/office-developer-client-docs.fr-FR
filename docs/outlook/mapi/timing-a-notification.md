---
title: Chronométrage d'une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360395"
---
# <a name="timing-a-notification"></a>Chronométrage d'une notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Étant donné que la notification d'événement est un processus asynchrone, vous pouvez être notifié à tout moment, pas nécessairement immédiatement après la survenue de l'événement.
  
 Le moment des appels à votre méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) varie en fonction du fournisseur de services qui implémente la source de notification. Les fournisseurs de services peuvent informer votre client: 
  
- En même temps que l'événement.
    
- Directement après l'événement.
    
- À un moment ultérieur, après l'événement, éventuellement après **** un appel Unadvise. 
    
La plupart des fournisseurs de services appellent **OnNotify** après que la méthode MAPI responsable de l'événement a renvoyé à son appelant. Par exemple, les notifications sur les messages sont envoyées lorsque les modifications apportées au message sont enregistrées, après l'appel de [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , ou lorsque le message est libéré, après l'appel **IUnknown:: Release** . Tant que la notification n'est pas envoyée, aucune modification n'est visible dans la Banque de messages. 
  
Vous pouvez recevoir des notifications à partir d'une source d' **** avis une fois que vous avez appelé Unadvise pour annuler une inscription. N'oubliez pas de libérer votre récepteur d'avertissement une fois que son nombre de références est tombé à zéro, **** et non à la suite d'un appel Unadvise réussi. Ne partez pas du principe que vous **** avez appelé Unadvise que le récepteur de notification n'est plus nécessaire. 
  

