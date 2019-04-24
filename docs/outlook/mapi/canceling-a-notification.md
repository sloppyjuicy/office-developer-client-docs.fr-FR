---
title: Annulation d'une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326403"
---
# <a name="canceling-a-notification"></a>Annulation d'une notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour annuler une notification, les clients appellent la méthode Unadvise de la source de notification. **** L' **** appel de Unadvise est important, car il permet au fournisseur de services de libérer sa référence à votre récepteur de notifications. Tant qu'un fournisseur de services gère une référence à un récepteur de notification, le récepteur de notifications peut continuer à recevoir des appels [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) . En fait, en raison de la nature asynchrone de la notification d'événement, les clients peuvent être avertis **** même après un appel Unadvise réussi. Les clients doivent être en mesure de gérer la réception des notifications à tout moment. 
  
Étant donné que les implémentations de fournisseur de services diffèrent **** , les clients qui ne peuvent pas appeler Unadvise pour annuler une notification ne peuvent pas supposer que le fournisseur libère sa référence à son récepteur de notification. Certains fournisseurs de services libèrent leurs références aux récepteurs de notification lorsqu'ils libèrent leurs sources de notification. Certains fournisseurs de services ne le font pas. Tant qu'un fournisseur de services gère une référence à un récepteur de notification, ce récepteur peut continuer à recevoir des notifications. 
  

