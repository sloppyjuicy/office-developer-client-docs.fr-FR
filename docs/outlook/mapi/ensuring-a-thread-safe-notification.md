---
title: Vérification de la notification thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424846"
---
# <a name="ensuring-a-thread-safe-notification"></a>Vérification de la notification thread-safe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si votre client s'exécute sur une plateforme multithread, vous aurez peut-être besoin de votre assurance que les appels à vos méthodes [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) se produisent sur un thread particulier. Étant donné que les appels vers **OnNotify** peuvent généralement se produire sur n'importe quel thread, il est possible de recevoir des notifications sur des threads inattendus et indésirables, conduisant à des erreurs difficiles à déboguer. 
  
Pour garantir que les appels vers **OnNotify** pour une notification particulière sont effectués sur le même thread que celui utilisé pour l'appel de la méthode Advise, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) avant d'appeler **** Advise. **** * * * * HrThisThreadAdviseSink * * * * crée un nouvel objet récepteur de notifications à partir de votre objet récepteur de Conseil. TransMettez ce nouvel objet dans l'appel **** à Advise. Tous les clients disposant de récepteurs de notifications qui risquent de ne pas fonctionner en dehors du contexte d'un thread particulier doivent toujours enregistrer les objets de récepteur d'avis créés avec **HrThisThreadAdviseSink**.
  

