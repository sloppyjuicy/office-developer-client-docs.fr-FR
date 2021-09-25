---
title: Garantie d’une Thread-Safe notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a0154e82227adc381b2e53cee47562be7ba3112b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601085"
---
# <a name="ensuring-a-thread-safe-notification"></a>Garantie d’une Thread-Safe notification

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si votre client s’exécute sur une plateforme multithread, vous devrez peut-être vous assurer que les appels à vos méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se produisent sur un thread particulier. Étant donné que les appels **à OnNotify** peuvent généralement se produire sur n’importe quel thread, il est possible de recevoir des notifications sur des threads inattendus et indésirables, entraînant des erreurs difficiles à déboguer. 
  
Pour garantir que les appels à **OnNotify** pour une notification particulière  sont effectués sur le même thread que celui utilisé pour l’appel de conseil, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) avant d’appeler **Advise**. ** **HrThisThreadAdviseSink**** crée un nouvel objet de sink de conseil à partir de votre objet de sink de conseil. Passez ce nouvel objet dans l’appel de **Advise**. Tous les clients avec des objets de sink de conseil qui peuvent ne pas fonctionner en dehors du contexte d’un thread particulier doivent toujours inscrire les objets de sink de conseil créés avec **HrThisThreadAdviseSink**.
  

