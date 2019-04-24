---
title: Fermeture d'une session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 74c2a7247df02570761247a9e4a6fae378f37312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287152"
---
# <a name="ending-a-mapi-session"></a>Fermeture d'une session MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients peuvent terminer leurs sessions en réponse à la demande d'un utilisateur, immédiatement ou après que tous les messages sortants ont été traités, et lorsqu'une erreur critique se produit. Certains clients doivent rester connectés afin que les messages sortants en attente puissent atteindre le fournisseur de transport et le système de messagerie de destination. Si un client de ce type envoie un message et se déconnecte immédiatement, le message peut rester dans la file d'attente sortante jusqu'à ce qu'un utilisateur se reconnecte et reste connecté suffisamment longtemps pour que le message soit transmis.
  
 **Lorsque vous devez terminer votre session avec le sous-système MAPI**
  
1. Annuler les inscriptions pour toutes les notifications en appelant **** la méthode Unadvise de chaque objet inscrit. 
    
2. Libérez tous les objets ouverts en appelant leurs méthodes [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) . Les types d'objets ouverts peuvent inclure des récepteurs de notification, la table d'État, le dossier boîte d'envoi, un ou plusieurs magasins de messages et le carnet d'adresses. 
    
3. Appelez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire pour les identificateurs d'entrée mis en cache, tels que **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. Appelez [IMAPISession:: Logoff](imapisession-logoff.md), en définissant l'indicateur MAPI_LOGOFF_UI si vous autorisez une interface utilisateur et l'indicateur MAPI_LOGOFF_SHARED si vous êtes propriétaire de la session partagée active. **** La déconnexion indique à tous les clients qui utilisent la session partagée active de se déconnecter en envoyant une notification d'erreur. 
    
5. Libérez le pointeur de session en appelant la méthode **IUnknown:: Release** de la session. 
    
6. Si vous avez appelé [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) pendant le démarrage de la session pour initialiser les bibliothèques OLE, ne l'initialisez pas maintenant en appelant [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx). Seuls les clients qui ont appelé **OleInitialize** doivent appeler **OleUninitialize**. 
    
7. Désinitialisez les bibliothèques MAPI en appelant [MAPIUninitialize](mapiuninitialize.md). Si vous avez appelé **OleInitialize** à un moment donné, assurez-vous qu'un appel à **OleUninitialize** se produit avant cet appel vers **MAPIUninitialize**. La synchronisation est essentielle. Si l'appel à **OleUninitialize** suit l'appel à **MAPIUninitialize**, votre client peut se terminer de manière inappropriée. 
    
8. Si vous avez appelé [ScInitMapiUtil](scinitmapiutil.md) pendant le démarrage de session pour initialiser la bibliothèque d'utilitaires MAPI, ne l'initialisez pas maintenant en appelant [DeinitMapiUtil](deinitmapiutil.md). Seuls les clients qui ont appelé **ScInitMapiUtil** doivent appeler **DeinitMapiUtil**.
    
> [!NOTE]
> Tous les objets ouverts doivent être libérés avant l'appel à **IMAPISession:: Logoff**. Les objets qui restent ouverts après la **fermeture de session** sont appelés deviennent non valides; ils ne peuvent pas accepter d'appels et ne peuvent jamais être libérés. Si un de ces objets est appelé, attendez-vous à ce que l'appel échoue. 
  
 MAPI n'a pas de mécanisme de suppression des dll pendant le processus d'arrêt de session. La DLL d'un fournisseur de services ne peut être supprimée que si un client de configuration tel que le panneau de configuration appelle sa fonction de point d'entrée de service de messagerie avec l'événement MSG_SERVICE_INSTALL. 
  

