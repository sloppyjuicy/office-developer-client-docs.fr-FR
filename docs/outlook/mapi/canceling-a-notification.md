---
title: Annulation d’une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
ms.openlocfilehash: 705e012ed735fc78ee055034259b49d018edf795
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372373"
---
# <a name="canceling-a-notification"></a>Annulation d’une notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour annuler une notification, les clients appellent la méthode **Unadvise d’une** source de conseil. Il **est important d’appeler Unadvise** , car le fournisseur de services libère sa référence à votre sink de conseil. Tant qu’un fournisseur de services maintient une référence à un réception de conseil, il peut continuer à recevoir des appels [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . En fait, en raison de la nature asynchrone de la notification d’événement, les clients peuvent être avertis même après un appel **Unadvise** réussi. Les clients doivent être en mesure de gérer la réception des notifications à tout moment. 
  
Étant donné que les implémentations des fournisseurs de services diffèrent, les clients qui ne parviennent pas à appeler **Unadvise** pour annuler une notification ne peuvent pas supposer le moment où un fournisseur publiera sa référence à son réception de notification. Certains fournisseurs de services publient leurs références pour conseiller les sinks lorsqu’ils libèrent leurs sources de conseil. Certains fournisseurs de services ne le font pas. Tant qu’un fournisseur de services conserve une référence à un receveur de notifications, ce dernier peut continuer à recevoir des notifications. 
  

