---
title: Annulation d’une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 50d1fb451cbfcd07f97c5b12a9c86c03a435faa6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564772"
---
# <a name="canceling-a-notification"></a>Annulation d’une notification

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour annuler une notification, les clients appellent **Unadvise** méthode d’une source advise. L’appel de **Unadvise** est important car le fournisseur de services libérer la référence à votre récepteur de notifications. Dans la mesure où un fournisseur de services gère une référence à un récepteur de notifications, le récepteur de notifications peut continuer à recevoir des appels [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . En fait, en raison de la nature de notification d’événement asynchrone, les clients peuvent être avertis même après une réussite **Unadvise** appeler. Clients doivent être en mesure de gérer la réception des notifications à tout moment. 
  
Comme les implémentations de fournisseur de service sont différents, les clients qui ont échoué pour appeler **Unadvise** pour annuler une notification ne peut pas supposez rien sur lorsqu’un fournisseur libère sa référence à leur récepteur de notifications. Certains fournisseurs de services libérer leurs références pour les récepteurs de notifications lorsque libèrent leurs sources advise. Certains fournisseurs de services ne mais pas. Dans la mesure où un fournisseur de services gère une référence à un récepteur de notifications, ce récepteur de notifications peut continuer à recevoir des notifications. 
  

