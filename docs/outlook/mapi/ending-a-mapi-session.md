---
title: Fin d’une session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
ms.openlocfilehash: c53fdbb73bd94889f0fd488c365bfbe673fae4cf
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380276"
---
# <a name="ending-a-mapi-session"></a>Fin d’une session MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients peuvent mettre fin à leurs sessions en réponse à la demande d’un utilisateur, immédiatement ou après le traitement de tous les messages sortants, et lorsqu’une erreur critique se produit. Certains clients doivent rester connectés afin que les messages sortants en attente peuvent atteindre le fournisseur de transport et le système de messagerie de destination. Si un tel client envoie un message et se déconnecte immédiatement, le message peut rester dans la file d’attente sortante jusqu’à ce qu’un utilisateur se connecte de nouveau et reste connecté suffisamment longtemps pour que le message soit transmis.
  
 **Lorsque vous devez mettre fin à votre session avec le sous-système MAPI**
  
1. Annulez les inscriptions pour toutes les notifications en appelant **la méthode Unadvise** de chaque objet inscrit. 
    
2. Ouvrez tous les objets ouverts en appelant leurs [méthodes IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) . Les types d’objets ouverts peuvent inclure des réceptions de conseil, la table d’état, le dossier Boîte d’envoi, un ou plusieurs magasins de messages et le carnet d’adresses. 
    
3. Appelez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire pour tous les identificateurs d’entrée mis en cache, tels que **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
4. Appelez [IMAPISession::Logoff](imapisession-logoff.md), en setting the MAPI_LOGOFF_UI flag if you allow a user interface and the MAPI_LOGOFF_SHARED flag if you own the current shared session. **La connexion avertit** tous les autres clients qui utilisent la session partagée actuelle qu’ils doivent se déconnecter en envoyant une notification d’erreur. 
    
5. Relâchez le pointeur de session en appelant la méthode **IUnknown::Release de la** session. 
    
6. Si vous avez appelé [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) au démarrage de la session pour initialiser les bibliothèques OLE, désinitialisez-les maintenant en appelant [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx). Seuls les clients qui ont **appelé OleInitialize** doivent appeler **OleUninitialize**. 
    
7. Désnitialiser les bibliothèques MAPI en appelant [MAPIUninitialize](mapiuninitialize.md). Si vous avez appelé **OleInitialize** à un moment donné, assurez-vous qu’un appel à **OleUninitialize** a lieu avant cet appel à **MAPIUninitialize**. Le minutage est crucial. Si l’appel à **OleUninitialize** suit l’appel de **MAPIUninitialize**, votre client peut s’interrompre de façon non réorganisable. 
    
8. Si vous avez appelé [ScInitMapiUtil](scinitmapiutil.md) au démarrage de la session pour initialiser la bibliothèque d’utilitaires MAPI, désinitialisez-la maintenant en appelant [DeinitMapiUtil](deinitmapiutil.md). Seuls les clients qui ont **appelé ScInitMapiUtil** doivent appeler **DeinitMapiUtil**.
    
> [!NOTE]
> Tous les objets ouverts doivent être libérés avant l’appel à **IMAPISession::Logoff**. Les objets qui restent ouverts après **l’appel de la logoff** deviennent non valides ; Ils ne peuvent accepter aucun appel et peuvent ne jamais être libérés. Si un appel est effectué vers l’un de ces objets, attendez-vous à ce que l’appel échoue. 
  
 MAPI ne dispose d’aucun mécanisme pour supprimer des DLL pendant le processus d’arrêt de session. La DLL d’un fournisseur de services ne peut être supprimée que lorsqu’un client de configuration tel que le Panneau de configuration appelle sa fonction de point d’entrée de service de message avec l’MSG_SERVICE_INSTALL de messagerie. 
  

