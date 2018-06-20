---
title: Implémentation d’objets Thread-Safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8c8c89f3626d54f04896ad54de5d7e480dd9b568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784214"
---
# <a name="implementing-thread-safe-objects"></a>Implémentation d’objets Thread-Safe

  
  
**S’applique à**: Outlook 
  
Avec les objets retournés par la méthode d’interface appelle directement, il incombe du fournisseur pour garantir la sécurité des threads. Avec les objets de rappel, c’est l’application cliente.
  
Un client peut implémenter un rappel de notification de thread-safe en appelant l’utilitaire MAPI [HrThisThreadAdviseSink](hrthisthreadadvisesink.md). **HrThisThreadAdviseSink** transforme un récepteur de notifications de thread-safe dans un thread-safe. Pour les rappels de progression, il n’existe pas d’utilitaire. Un client peut choisir d’utiliser l’objet de l’avancement du thread-safe MAPI ou en créer une manuellement. 
  
Un objet thread-safe peut ou non également être thread prenant en charge. Un objet prenant en charge les threads gère un contexte distinct pour chaque thread qui est à l’aide. Fournisseurs de services ne sont pas nécessaire pour prendre en charge de thread-sensibilisation dans leurs objets thread-safe, bien que la prise en charge de sensibilisation à la thread peut être utile dans certaines situations. Deux tables MAPI toujours fournissent leur propre contexte par définition. Une table utilisée sur différents threads ne pas et ne doit pas fournir de contexte unique.
  
Un client peut choisir de recevoir des notifications sur le même thread qui a été utilisé pour l' **exécuter MAPIInitialize** appeler, sur le même thread qui a été utilisé pour l’appel **Advise** , soit sur un thread distinct détenus par MAPI. Pour vous assurer que les notifications arrivent sur le même thread qui a servi à **exécuter MAPIInitialize**d’appel, un client appelle [exécuter MAPIInitialize](mapiinitialize.md) et transmet la valeur zéro dans le membre **ulFlags** de la structure [MAPIINIT_0](mapiinit_0.md) . Les notifications sont ensuite remises au cours de la boucle de message principale. 
  
Pour recevoir des notifications sur le thread appartenant à MAPI, un client appelle **exécuter MAPIInitialize** avec le membre **ulFlags** de la structure **MAPIINIT_0** défini sur MAPI_MULTITHREAD_NOTIFICATIONS. L’appel **Advise** est effectuée avec objet récepteur plutôt que sur une version encapsulée de notification du client. 
  
Pour vous assurer que les notifications arrivent sur le même thread qui a été utilisé pour appeler **Advise**, un client appelle [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) et passe encapsulé nouvellement créé de notification récepteur **Advise** plutôt que le récepteur de notifications d’origine. **Exécuter MAPIInitialize** peut être appelée avec une valeur d’indicateur. 
  

