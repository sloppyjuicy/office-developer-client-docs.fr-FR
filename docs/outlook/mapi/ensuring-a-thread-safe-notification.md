---
title: Garantie d'Thread-Safe notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
ms.openlocfilehash: 195111c6b16271b350e1d162399677efefed75b5
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405291"
---
# <a name="ensuring-a-thread-safe-notification"></a>Garantie d'Thread-Safe notification

**S’applique à** : Outlook 2013 | Outlook 2016
  
Si votre client s’exécute sur une plateforme multithread, vous devrez peut-être vous assurer que les appels à vos méthodes [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) se produisent sur un thread particulier. Étant donné que les appels **à OnNotify** peuvent généralement se produire sur n’importe quel thread, il est possible de recevoir des notifications sur des threads inattendus et indésirables, entraînant des erreurs difficiles à déboguer.
  
Pour garantir que les appels à **OnNotify** pour une notification particulière sont effectués sur le même thread que celui utilisé  pour l’appel de conseil, appelez [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) avant d’appeler **Advise**. **HrThisThreadAdviseSink** crée un objet de sink de conseil à partir de votre objet de sink de conseil. Passez ce nouvel objet dans l’appel au **conseiller**. Tous les clients avec des objets de sink de conseil qui peuvent ne pas fonctionner en dehors du contexte d’un thread particulier doivent toujours inscrire les objets de sink de conseil créés avec **HrThisThreadAdviseSink**.
