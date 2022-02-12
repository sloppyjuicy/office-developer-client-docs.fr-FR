---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b180d1d9e6823a299764475722a547a9c38189c8
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781330"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder aux informations de la boutique de messages et aux messages et dossiers.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objet de magasin de messages  <br/> |
|Implémenté par :  <br/> |Fournisseurs de magasins de messages  <br/> |
|Appelé par :  <br/> |Applications clientes, lepooler MAPI et MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMsgStore  <br/> |
|Type de pointeur :  <br/> |LPMDB  <br/> |
|Modèle de transaction :  <br/> |Non traduit  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[Conseiller](imsgstore-advise.md) <br/> |S’inscrit pour recevoir une notification des événements spécifiés qui affectent la boutique de messages. |
|[Unadvise](imsgstore-unadvise.md) <br/> |Annule l’envoi de notifications précédemment définies avec un appel à la **méthode IMsgStore::Advise** . |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence à la même entrée dans une magasin de messages. |
|[OpenEntry](imsgstore-openentry.md) <br/> |Ouvre un dossier ou un message et renvoie un pointeur d’interface pour un accès supplémentaire. |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Établit un dossier comme destination pour les messages entrants d’une classe de message particulière. |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Obtient le dossier qui a été établi comme destination pour les messages entrants d’une classe de message spécifiée ou comme dossier de réception par défaut pour la magasin de messages. |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Permet d’accéder à la table des dossiers de réception, une table contenant des informations sur tous les dossiers de réception de la boutique de messages. |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Active la ff de logo dans l’ordre de la boutique de messages. |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Tente de supprimer un message de la file d’attente sortante. |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Permet d’accéder à la table de files d’attente sortante, une table qui contient des informations sur tous les messages de la file d’attente sortante de la boutique de messages. |
|[SetLockState](imsgstore-setlockstate.md) <br/> |Verrouille ou déverrouille un message. |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Permet au fournisseur de magasin de messages d’effectuer un traitement sur un message envoyé. |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |Informe la banque de messages un nouveau message est arriv�. |
   
|**Propriétés requises**|**Niveau d’accès**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
Les propriétés suivantes sont pour les magasins de messages interpersonnels (IPM) :
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)

