---
title: Mise en œuvre Thread-Safe objets
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bf3b3e9dddaeb09a15ab658b6a6cd6d8447c4140
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630543"
---
# <a name="implementing-thread-safe-objects"></a>Mise en œuvre Thread-Safe objets

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avec les objets qui sont renvoyés directement par les appels de méthode d’interface, il incombe au fournisseur de garantir la sécurité des threads. Avec les objets de rappel, c’est la responsabilité de l’application cliente.
  
Un client peut implémenter un rappel de notification thread-safe en appelant l’utilitaire MAPI [HrThisThreadAdviseSink](hrthisthreadadvisesink.md). **HrThisThreadAdviseSink** transforme un sink de conseil non thread-safe en un sink thread-safe. Pour les rappels de progression, il n’existe aucun utilitaire de ce type. Un client peut choisir d’utiliser l’objet de progression thread-safe MAPI ou d’en créer un manuellement. 
  
Un objet thread-safe peut ou non être également pris en compte par les threads. Un objet thread-aware conserve un contexte distinct pour chaque thread qui l’utilise. Les fournisseurs de services ne sont pas obligés de prendre en charge la prise en charge de la prise en charge des threads dans leurs objets thread-safe, bien que la prise en charge de la prise en charge de la prise en charge des threads puisse être utile dans certaines situations. Deux tables MAPI fournissent toujours leur propre contexte par définition. Une table utilisée sur différents threads ne fournit pas et ne doit pas fournir de contexte unique.
  
Un client peut choisir entre la réception de notifications sur le même thread que celui utilisé pour  l’appel **MAPIInitialize,** sur le même thread que celui utilisé pour l’appel de notification ou sur un thread distinct qui appartient à MAPI. Pour s’assurer que les notifications arrivent sur le même thread que celui utilisé pour appeler **MAPIInitialize,** un client appelle [MAPIInitialize](mapiinitialize.md) et transmet zéro dans le membre **ulFlags** de la structure [MAPIINIT_0.](mapiinit_0.md) Les notifications sont ensuite remis pendant la boucle de message principale. 
  
Pour recevoir des notifications sur le thread MAPI, un client appelle **MAPIInitialize** avec le membre **ulFlags** de la structure **MAPIINIT_0** définie sur MAPI_MULTITHREAD_NOTIFICATIONS. **L’appel** de conseil est effectué avec l’objet de sink de conseil du client au lieu d’une version wrapped. 
  
Pour s’assurer que les notifications arrivent sur le même thread que celui utilisé pour appeler **Advise,** un client appelle [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) et transmet le nouveau reçu de conseil wrapped à **Advise** plutôt qu’au sink de notification d’origine. **MAPIInitialize peut** être appelé avec l’une ou l’autre valeur d’indicateur. 
  

