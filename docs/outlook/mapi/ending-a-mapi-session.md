---
title: Mettre fin à une Session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 844880e5a1e40b51ece30baafd969372e7d43121
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783251"
---
# <a name="ending-a-mapi-session"></a>Mettre fin à une Session MAPI

  
  
**S’applique à**: Outlook 
  
Les clients peuvent mettre fin à leurs sessions en réponse à une demande d’un utilisateur, soit immédiatement ou sortants une fois que tous les messages ont été traités et quand se produit une erreur critique. Certains clients ont besoin de rester connecté afin que les messages sortants en attente peut atteindre le fournisseur de transport et la système de messagerie de destination. Si un tel client envoie un message et déconnecte immédiatement, le message peut rester dans la file d’attente sortante jusqu'à ce qu’un utilisateur se reconnecte et reste connecté suffisamment longtemps pour que le message peut être transmis.
  
 **Lorsque vous devez mettre fin à votre session avec le sous-système MAPI**
  
1. Annuler les enregistrements pour toutes les notifications en appelant la méthode **Unadvise** de chaque objet inscrit. 
    
2. Libérer tous les objets ouverts en appelant leurs méthodes [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) . Les types d’objets ouverts peuvent inclure de notification récepteurs de la table d’état, le dossier boîte d’envoi, une ou plusieurs bases de messages et le carnet d’adresses. 
    
3. Appelez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire pour les identificateurs d’entrée mise en cache, telles que **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. [IMAPISession::Logoff](imapisession-logoff.md), définition de l’indicateur MAPI_LOGOFF_UI si vous autorisez une interface utilisateur et l’indicateur MAPI_LOGOFF_SHARED si vous possédez la session partagée en cours d’appel. **Fermeture de session** avertit tous les autres clients qui utilisent la session partagée active, ils doivent se déconnectent en envoyant une notification d’erreur. 
    
5. Libérer le pointeur de la session en appelant la méthode **IUnknown::Release** de la session. 
    
6. Si vous avez appelé [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) lors du démarrage de session pour initialiser les bibliothèques OLE, initialiser les maintenant en appelant [OleUninitialize](http://msdn.microsoft.com/en-us/library/ms691326%28VS.85%29.aspx). Seuls les clients qui ont appelé **OleInitialize** doivent appeler **OleUninitialize**. 
    
7. Annuler l’initialisation en appelant [MAPIUninitialize](mapiuninitialize.md)les bibliothèques de MAPI. Si vous avez appelé **OleInitialize** à un moment donné, assurez-vous qu’un appel à **OleUninitialize** se produit avant cet appel à **MAPIUninitialize**. La synchronisation est essentielle. Si l’appel à **OleUninitialize** suit l’appel **MAPIUninitialize**, votre client peut interrompre échouaient. 
    
8. Si vous avez appelé [ScInitMapiUtil](scinitmapiutil.md) lors du démarrage de session pour initialiser la bibliothèque d’utilitaires MAPI, annuler l’initialisation en maintenant en appelant [DeinitMapiUtil](deinitmapiutil.md). Seuls les clients qui ont appelé **ScInitMapiUtil** doivent appeler **DeinitMapiUtil**.
    
> [!NOTE]
> Tous les objets ouverts doivent être libérés avant l’appel à **IMAPISession::Logoff**. Les objets qui restent ouverts après la **fermeture de session** est appelé deviennent non valides ; ils ne peut pas accepter des appels et ne peuvent jamais être libérées. Si un appel est effectué à un de ces objets, attendez l’appel échoue. 
  
 MAPI n’a aucun mécanisme de suppression des DLL au cours du processus de fermeture de session. Service que DLL du fournisseur peut être supprimée uniquement lorsqu’un client de configuration tels que le panneau de configuration appelle la fonction point d’entrée message service avec l’événement MSG_SERVICE_INSTALL. 
  

