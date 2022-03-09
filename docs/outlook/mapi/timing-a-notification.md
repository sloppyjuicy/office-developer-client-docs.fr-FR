---
title: Minutage d’une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
ms.openlocfilehash: e58fba179d13662cfc9a1533a5481a9a06c3e615
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375369"
---
# <a name="timing-a-notification"></a>Minutage d’une notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Étant donné que la notification d’événement est un processus asynchrone, vous pouvez être averti à tout moment, pas nécessairement immédiatement après que l’événement s’est produit.
  
 Le délai des appels à votre méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varie en fonction du fournisseur de services qui implémente la source de conseil. Les fournisseurs de services peuvent notifier votre client : 
  
- Simultanément avec l’événement.
    
- Directement après l’événement.
    
- À un moment ultérieur suivant l’événement, éventuellement après un **appel Unadvise** . 
    
La plupart des fournisseurs de services **appellent OnNotify** une fois que la méthode MAPI responsable de l’événement est retournée à son appelant. Par exemple, les notifications sur les messages sont envoyées lorsque les modifications apportées au message sont enregistrées, après l’appel [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , ou lorsque le message est libéré, après l’appel **IUnknown::Release** . Tant que la notification n’est pas envoyée, aucune modification n’est visible dans la boutique de messages. 
  
Vous pouvez recevoir des notifications d’une source de conseil après avoir appelé **Unadvise** pour annuler une inscription. N’oubliez pas de libérer votre sink de conseil uniquement une fois que son nombre de références est passé à zéro, sans suivre un appel **Unadvise** réussi. Ne supposez pas que, étant donné que vous avez appelé **Unadvise,** le sink de conseil n’est plus nécessaire. 
  

