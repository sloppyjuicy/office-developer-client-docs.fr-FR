---
title: Une Notification de temporisation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9ee999841b53f358dcee85d4d92c5056f665dbf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787352"
---
# <a name="timing-a-notification"></a>Une Notification de temporisation

  
  
**S’applique à**: Outlook 
  
Notification d’événement étant un processus asynchrone, vous pouvez être averti à tout moment, pas nécessairement immédiatement après que l’événement s’est produite.
  
 La durée des appels à votre méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) varie selon le fournisseur de services l’implémentation de la source de notification. Fournisseurs de services peuvent informer votre client soit : 
  
- Simultanément avec l’événement.
    
- Directement après l’événement.
    
- À plus tard un moment donné à la suite de l’événement, éventuellement après un appel **Unadvise** . 
    
La plupart des fournisseurs de services d’appel **OnNotify** après que la méthode MAPI responsable de l’événement a renvoyé à l’appelant. Par exemple, les notifications sur les messages sont envoyées lorsque des modifications apportées au message sont enregistrées, après l’appel de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , ou lorsque le message est lancé, après l’appel **IUnknown::Release** . Jusqu'à ce que la notification est envoyée, aucune modification n’est visible dans la banque de messages. 
  
Vous pouvez recevoir des notifications à partir d’une source advise après avoir appelé **Unadvise** pour annuler l’inscription d’une. Veillez à libérer votre récepteur de notifications qu’après que son décompte de références est réduit à zéro, un appel réussi de **Unadvise** ne pas suivant. Ne supposent que parce que vous avez appelé **Unadvise** le récepteur de notifications n’est plus nécessaire. 
  

