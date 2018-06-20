---
title: L’ouverture d’un dossier de la banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 63b8224ad56e2b9985c9d733e2a3c27c67eb2f7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784932"
---
# <a name="opening-a-message-store-folder"></a>L’ouverture d’un dossier de la banque de messages

**S’applique à**: Outlook 
  
Avant de n’importe quel dossier peut être ouverts, son identificateur d’entrée doit être disponible. Pour la plupart des dossiers, cela signifie récupérer leurs propriétés **PR_ENTRYID** . Pour les dossiers spéciaux, tels que les dossiers de la sous-arborescence IPM et autres dossiers racine, MAPI définit propriétés d’identificateur d’entrée qui sont accessibles en appelant la méthode de **IMAPIProp::GetProps** de la banque de messages. Ces identificateurs d’entrée sont toujours à long terme et sont nommés comme suit : 
  
|**Folder**|**Propriété identificateur**|
|:-----|:-----|
|Dossier bo�te d'envoi  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (Classe de message IPM)  <br/> |
|Dossier �l�ments supprim�s  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|dossier �l�ments envoy�s  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|Dossier racine IPM  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Dossier racine de r�sultats de recherche  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Dossier racine de vues commun  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Dossier racine de vues personnelles  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Dossier racine de contacts  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Dossier racine de brouillons  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Dossier racine de journal  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Dossier racine de calendrier  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Dossier racine de notes  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Dossier racine de tâches  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Avant d’essayer de récupérer l’une de ces identificateurs d’entrée, récupérer le **PR\_VALID_FOLDER_MASK** propriété ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) de la banque de messages. **PR\_VALID_FOLDER_MASK** est un masque de bits qui identifie les identificateurs existent de l’entrée. Il existe un bit pour chacun des dossiers spéciaux. Si le bit est activé, il indique que le dossier correspondant est pris en charge et qu’il possède un identificateur d’entrée valide. Par exemple, si le dossier éléments supprimés existe et qu’il possède un identificateur d’entrée valide, le dossier\_IPM_WASTEBASKET_VALID bits sera définie dans **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Ouvrez le dossier dans lequel sont placés tous les messages entrants d’une classe particulière
  
1. Appelez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer son identificateur d’entrée, la définition du paramètre _lpszMessageClass_ pour pointer vers une chaîne de caractères qui identifie la classe de message. Par exemple, si vous souhaitez ouvrir la boîte de réception pour la sous-arborescence IPM, pointez _lpszMessageClass_ IPM. Si vous souhaitez ouvrir le dossier de réception des messages IPC, définissez qu’elle pointe vers IPC. 

   S’il n’existe aucun dossier de réception inscrits pour la classe de message, **GetReceiveFolder** choisit le dossier de réception dont la classe de message associé établit une correspondance avec le préfixe le plus longtemps possible de la classe de message passé. Pour plus d’informations, voir [MAPI recevoir des dossiers](mapi-receive-folders.md). 
   
   Notez que la propriété **PR_IPM_OUTBOX_ENTRYID** est utilisée pour ouvrir le dossier boîte d’envoi uniquement pour les messages IPM. Si vous ouvrez la boîte d’envoi des messages IPC, utilisez plutôt l’identificateur d’entrée de son dossier de réception. Les messages entrants et sortants IPC sont placés dans le dossier de réception. 
    
2. Appelez un des quatre méthodes **OpenEntry** pour ouvrir le dossier et retourne un pointeur d’interface qui vous permet d’y accéder. Vous pouvez appeler l’une des méthodes suivantes pour ouvrir un dossier : 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   La méthode spécifique que vous choisissez dépend du dossier à ouvrir et les objets qui sont disponibles au moment. Étant donné que la méthode **IMAPISession** peut ouvrir n’importe quel dossier pour les messages dans le profil actuel, appelez cette **OpenEntry** lorsque vous ne savez pas quoi que ce soit sur le dossier à ouvrir. Si vous connaissez lesquelles messages possède le dossier et que vous avez un pointeur vers la banque de messages, appelez **IMsgStore::OpenEntry**. 
    
   Par exemple, utilisez la méthode **IMsgStore** pour ouvrir un dossier de réception. Si vous avez un pointeur vers l’objet d’ouverture de session du fournisseur de banque de messages, appelez **IMSLogon::OpenEntry**. Étant donné que ces appels aller directement vers le fournisseur de banque de messages plutôt que par le biais de MAPI, le traitement est plus rapide. Si le dossier que vous ouvrez est un sous-dossier d’un dossier que vous avez déjà ouvert, appeler la méthode de **IMAPIContainer::OpenEntry** du dossier ouvert. La méthode **IMAPIContainer** uniquement les sous-dossiers d’un dossier actuellement ouvert s’ouvre et est la seule méthode pour travailler avec les identificateurs d’entrée à court terme. 
    
3. Si vous souhaitez être en mesure d’apporter des modifications dans le dossier à ouvrir, spécifiez un niveau d’accès en définissant la soit MAPI\_meilleures\_ACCESS ou MAPI\_indicateur modifier dans l’appel de **OpenEntry** . Ces indicateurs sont des suggestions pour le fournisseur de banque de messages pour accorder le niveau d’accès, le plus élevé pour MAPI\_meilleures\_ou accès en lecture/écriture, pour MAPI\_modifier, lors de l’ouverture du dossier. 

   Étant donné que ces indicateurs ne sont que des propositions, le dossier peut ou ne peut pas être ouvert avec le niveau d’accès souhaité. En récupérant la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), vous pouvez déterminer la plage d’opérations qui peuvent être effectuées dans le dossier ouvert. 
    
   Toutefois, étant donné que de nombreux fournisseurs de banque de messages calculer la valeur de cette propriété sur la demande, plutôt qu’il prise en charge sous la forme d’une propriété de dossier ou en tant que colonne dans leur table de hiérarchie, récupérer peut prendre du temps. Une autre stratégie consiste à essayer de toute opération, vous devez effectuer et renvoie une erreur si nécessaire.
    
## <a name="see-also"></a>Voir aussi

- [Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

