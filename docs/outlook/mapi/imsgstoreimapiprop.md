---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4ed17fd7f826432da9460fe01e5aa76802726bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584631"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder aux informations de banque de messages et aux messages et des dossiers.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objet store de message  <br/> |
|Implémenté par :  <br/> |Fournisseurs de banque de messages  <br/> |
|Appelé par :  <br/> |Applications clientes, le spouleur MAPI et MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMsgStore  <br/> |
|Type de pointeur :  <br/> |IPMDB  <br/> |
|Modèle de transaction :  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Conseiller](imsgstore-advise.md) <br/> |Inscrit pour recevoir des notifications d’événements spécifiques qui affectent la banque de messages.  <br/> |
|[L’avertissement](imsgstore-unadvise.md) <br/> |Annule l’envoi de notifications précédemment configurées avec un appel à la méthode **IMsgStore::Advise** .  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer si elles font référence à la même entrée dans une banque de messages.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Ouvre un dossier ou un message et retourne un pointeur d’interface pour l’accès des autres.  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |Établissement d’un dossier comme destination pour les messages entrants d’une classe de message particulier.  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |Obtient le dossier qui a été établi comme dossier pour la banque de messages de réception de la destination pour les messages entrants d’une classe de message spécifié ou en tant que la valeur par défaut.  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |Permet d’accéder à la table de dossier de réception, un tableau avec des informations sur tous les dossiers de réception de la banque de messages.  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |Permet la déconnexion ordonnée de la banque de messages.  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |Tente de supprimer un message de la file d’attente sortante.  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |Permet d’accéder à la table sortant de la file d’attente, une table qui comporte des informations sur tous les messages en file d’attente sortante de la banque de messages.  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |Verrouiller ou déverrouiller un message.  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |Active le fournisseur de banque de messages effectuer le traitement sur un message envoyé.  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |Informe la banque de messages un nouveau message est arriv�.  <br/> |
   
|**Propriétés requises**|**Niveau d’accès**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
Les propriétés suivantes sont des magasins de message message interpersonnel (IPM) :
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)

