---
title: Garantir une notification thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ad10b2ebd835b21f207fd43ecd8aebc7e1f475f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585303"
---
# <a name="ensuring-a-thread-safe-notification"></a>Garantir une notification thread-safe

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Si votre client s’exécute sur une plate-forme multithread, vous devrez peut-être pour l’assurance que les appels vers les méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se produisent sur un thread particulier. Étant donné que les appels vers **OnNotify** peuvent se produire généralement sur n’importe quel thread, il est possible de recevoir des notifications sur des threads inattendus et indésirables conduisant à des erreurs sont difficiles à déboguer. 
  
Afin de garantir que les appels vers **OnNotify** pour une notification particulier sont effectuées sur le même thread qui a été utilisé pour les **notifications** d' appel, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) avant d’appeler des **notifications**. ** ** HrThisThreadAdviseSink *** crée un nouvel objet de récepteur de notifications à partir de votre objet de récepteur advise. Transmettez ce nouvel objet dans l’appel à **Advise**. Tous les clients avec des objets qui risque de ne pas fonctionner en dehors du contexte d’un thread particulier doivent toujours enregistrer de récepteur de notifications de notification objets récepteur créés avec **HrThisThreadAdviseSink**.
  

