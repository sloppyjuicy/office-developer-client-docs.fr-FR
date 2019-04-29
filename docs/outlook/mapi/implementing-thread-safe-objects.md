---
title: Implémentation d'objets thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9160136542c7960bad0be2423872171b17d99fe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413527"
---
# <a name="implementing-thread-safe-objects"></a>Implémentation d'objets thread-safe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avec les objets qui sont renvoyés à partir des appels de méthode d'interface directement, il incombe au fournisseur de s'assurer de la sécurité des threads. Avec les objets callback, il s'agit de la responsabilité de l'application cliente.
  
Un client peut implémenter un rappel de notification thread-safe en appelant l'utilitaire MAPI [HrThisThreadAdviseSink](hrthisthreadadvisesink.md). **HrThisThreadAdviseSink** transforme un récepteur de conseillers non thread-safe en un récepteur thread-safe. Pour les rappels de progression, il n'existe pas d'utilitaire de ce type. Un client peut choisir d'utiliser l'objet de progression thread-safe MAPI ou d'en créer un manuellement. 
  
Un objet thread-safe peut également ou non être pris en charge par les threads. Un objet lié à un thread gère un contexte distinct pour chaque thread qui l'utilise. Les fournisseurs de services ne sont pas tenus de prendre en charge la détection des threads dans leurs objets thread-safe, bien que la prise en charge de la détection des threads puisse être utile dans certaines situations. Deux tables MAPI fournissent toujours leur propre contexte par définition. Une table utilisée sur des threads différents ne doit pas fournir de contexte unique.
  
Un client peut choisir entre recevoir des notifications sur le même thread que celui utilisé pour l'appel **MAPIInitialize** , sur le même thread que celui utilisé pour l'appel de la fonction Advise ou sur un thread distinct appartenant à MAPI. **** Pour vous assurer que les notifications arrivent sur le même thread que celui utilisé pour appeler **MAPIInitialize**, un client appelle [MAPIInitialize](mapiinitialize.md) et transmet zéro dans le membre **ulFlags** de la structure [MAPIINIT_0](mapiinit_0.md) . Les notifications sont ensuite remises lors de la boucle de message principale. 
  
Pour recevoir des notifications sur le thread appartenant à MAPI, un client appelle **MAPIInitialize** avec le membre **ulFlags** de la structure **MAPIINIT_0** définie sur MAPI_MULTITHREAD_NOTIFICATIONS. L' **** appel de la fonction Advise est effectué avec l'objet de récepteur de notification du client au lieu d'une version enveloppée. 
  
Pour vous assurer que les notifications arrivent sur le même thread que celui **** utilisé pour appeler Advise, un client appelle [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) et transmet le récepteur de notifications renvoyées nouvellement créé à des **conseils** au lieu du récepteur de notification d'origine. **MAPIInitialize** peut être appelé avec n'importe quelle valeur d'indicateur. 
  

