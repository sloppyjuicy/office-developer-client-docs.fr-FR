---
title: Ouverture d’un dossier d’une banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: df7db013cb435484c721388abab51ab4ba43828f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331373"
---
# <a name="opening-a-message-store-folder"></a>Ouverture d’un dossier d’une banque de messages

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour pouvoir ouvrir un dossier, son identificateur d'entrée doit être disponible. Pour la plupart des dossiers, cela signifie que vous récupérez leurs propriétés **PR_ENTRYID** . Pour les dossiers spéciaux, tels que les dossiers de sous-arborescence IPM et d'autres dossiers racine, MAPI définit des propriétés d'identificateur d'entrée spéciales qui sont accessibles en appelant la méthode **IMAPIProp:: GetProps** de la Banque de messages. Ces identificateurs d'entrée sont toujours à long terme et sont nommés comme suit: 
  
|**Folder**|**Propriété d'identificateur d'entrée**|
|:-----|:-----|
|Dossier bo�te d'envoi  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (Classe de message IPM uniquement)  <br/> |
|dossier Éléments supprimés  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|dossier �l�ments envoy�s  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|Dossier racine IPM  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Dossier racine de r�sultats de recherche  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Dossier racine des affichages communs  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Dossier racine des affichages personnels  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Dossier racine des contacts  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Dossier racine des brouillons  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Dossier racine de journal  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Dossier racine du calendrier  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Dossier racine des notes  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Dossier des tâches racine  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Avant d'essayer de récupérer l'un de ces identificateurs d'entrée spéciaux, récupérez la propriété **\_PR VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) de la Banque de messages. **PR\_VALID_FOLDER_MASK** est un masque de qui identifie les identificateurs d'entrée spéciaux qui existent. Il y a un bit pour chaque dossier spécial. Si le bit est défini, il indique que le dossier correspondant est pris en charge et possède un identificateur d'entrée valide. Par exemple, si le dossier éléments supprimés existe et qu'il possède un identificateur d'entrée valide,\_le IPM_WASTEBASKET_VALID de dossier est défini dans **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Ouvrir le dossier dans lequel sont placés tous les messages entrants d'une classe particulière
  
1. Appelez [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer son identificateur d'entrée, en définissant le paramètre _lpszMessageClass_ de sorte qu'il pointe vers une chaîne de caractères identifiant la classe de message. Par exemple, si vous souhaitez ouvrir la boîte de réception de votre sous-arborescence IPM, pointez _lpszMessageClass_ vers IPM. Si vous souhaitez ouvrir le dossier de réception pour les messages IPC, définissez-le sur IPC. 

   S'il n'existe aucun dossier de réception enregistré pour la classe de message, **GetReceiveFolder** choisit le dossier de réception dont la classe de message associée correspond au préfixe le plus long possible de la classe de message passée. Pour plus d'informations, consultez la rubrique [MAPI Receive Folders](mapi-receive-folders.md). 
   
   Notez que la propriété **PR_IPM_OUTBOX_ENTRYID** est utilisée pour ouvrir le dossier boîte d'envoi uniquement pour les messages IPM. Si vous ouvrez la boîte d'envoi pour les messages IPC, utilisez à la place l'identificateur d'entrée pour le dossier de réception. Les messages IPC entrants et sortants sont placés dans le dossier de réception. 
    
2. Appelez l'une des quatre méthodes **OpenEntry** pour ouvrir le dossier et retourner un pointeur d'interface que vous pouvez utiliser pour y accéder. Vous pouvez appeler l'une des méthodes suivantes pour ouvrir un dossier: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   La méthode spécifique que vous choisissez dépend du dossier à ouvrir et des objets disponibles en même temps. Étant donné que la méthode **IMAPISession** peut ouvrir n'importe quel dossier pour n'importe quel magasin de messages dans le profil actuel, appelez cette **OpenEntry** lorsque vous ne savez pas quoi faire pour ouvrir le dossier. Si vous identifiez la Banque de messages propriétaire du dossier et que vous disposez d'un pointeur vers la Banque de messages, appelez **IMsgStore:: OpenEntry**. 
    
   Par exemple, utilisez la méthode **IMsgStore** pour ouvrir un dossier de réception. Si vous avez un pointeur vers l'objet d'ouverture de session du fournisseur de banque de messages, appelez **IMSLogon:: OpenEntry**. Étant donné que ces appels sont directement dirigés vers le fournisseur de banque de messages plutôt que via MAPI, le traitement est plus rapide. Si le dossier que vous ouvrez est un sous-dossier d'un dossier que vous avez déjà ouvert, appelez la méthode **IMAPIContainer:: OpenEntry** du dossier Open. La méthode **IMAPIContainer** ouvre uniquement les sous-dossiers d'un dossier actuellement ouvert et est la seule méthode garantis d'utiliser des identificateurs d'entrée à court terme. 
    
3. Si vous souhaitez pouvoir modifier le dossier, spécifiez un niveau d'accès en définissant l'indicateur\_MAPI Best\_Access ou MAPI\_Modify dans l'appel **OpenEntry** . Ces indicateurs sont des suggestions pour le fournisseur de banque de messages afin d'accorder le niveau d'accès\_\_le plus élevé pour l'accès MAPI, ou l'accès\_en lecture/écriture pour MAPI, lors de l'ouverture du dossier. 

   Ces indicateurs étant uniquement des suggestions, il se peut que le dossier soit ouvert ou non avec le niveau d'accès attendu. En récupérant la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), vous pouvez déterminer la plage d'opérations qui peut être effectuée sur le dossier ouvert. 
    
   Toutefois, étant donné que de nombreux fournisseurs de banques de messages calculent la valeur de cette propriété à la demande plutôt qu'en tant que propriété de dossier ou en tant que colonne dans leur table de hiérarchie, la récupération peut prendre du temps. Une autre stratégie consiste à essayer toutes les opérations que vous devez effectuer et renvoyer une erreur si nécessaire.
    
## <a name="see-also"></a>Voir aussi

- [Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

