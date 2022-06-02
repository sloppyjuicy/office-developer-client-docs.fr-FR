---
title: Ouverture d’un dossier d’une banque de messages
description: Décrit les dossiers et propriétés de l’identificateur d’entrée, qui doivent être disponibles avant que n’importe quel dossier puisse être ouvert.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
ms.openlocfilehash: 005280afe9c45ca1309c09b738d1f513a222036d
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852396"
---
# <a name="opening-a-message-store-folder"></a>Ouverture d’un dossier d’une banque de messages

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant de pouvoir ouvrir un dossier, son identificateur d’entrée doit être disponible. Pour la plupart des dossiers, cela signifie récupérer leurs propriétés **de PR_ENTRYID** . Pour les dossiers spéciaux, tels que certains dossiers de sous-arborescence IPM et d’autres dossiers racine, MAPI définit des propriétés d’identificateur d’entrée spéciales accessibles en appelant la méthode **IMAPIProp::GetProps** du magasin de messages. Ces identificateurs d’entrée sont toujours à long terme et sont nommés comme suit : 
  
|**Folder**|**Propriété d’identificateur d’entrée**|
|:-----|:-----|
|Dossier bo�te d'envoi  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (classe de message IPM uniquement)  <br/> |
|dossier Éléments supprimés  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|dossier �l�ments envoy�s  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|Dossier racine IPM  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Dossier racine de r�sultats de recherche  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Dossier racine des vues courantes  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Dossier racine des vues personnelles  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Dossier racine contacts  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Brouillons du dossier racine  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Dossier racine du journal  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Dossier racine du calendrier  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Dossier racine notes  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Dossier racine des tâches  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Avant d’essayer de récupérer l’un de ces identificateurs d’entrée spéciaux, récupérez la **\_propriété pr VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) du magasin de messages. **PR\_ VALID_FOLDER_MASK** est un masque de bits qui identifie lequel des identificateurs d’entrée spéciaux existe. Il existe un bit pour chacun des dossiers spéciaux. Si le bit est défini, il indique que le dossier correspondant est pris en charge et qu’il a un identificateur d’entrée valide. Par exemple, si le dossier Éléments supprimés existe et a un identificateur d’entrée valide, le IPM_WASTEBASKET_VALID bit FOLDER\_est défini dans **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Ouvrez le dossier dans lequel tous les messages entrants d’une classe particulière sont placés
  
1. Appelez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer son identificateur d’entrée, en définissant le paramètre  _lpszMessageClass_ pour qu’il pointe vers une chaîne de caractères identifiant la classe de message. Par exemple, si vous souhaitez ouvrir la boîte de réception de votre sous-arborescence IPM, pointez  _lpszMessageClass_ sur IPM. Si vous souhaitez ouvrir le dossier de réception pour les messages IPC, définissez-le pour qu’il pointe vers IPC. 

   S’il n’existe aucun dossier de réception inscrit pour la classe de message, **GetReceiveFolder** choisit le dossier de réception dont la classe de message associée correspond au préfixe le plus long possible de la classe de message passée. Pour plus d’informations, consultez [Dossiers de réception MAPI](mapi-receive-folders.md). 
   
   Notez que la propriété **PR_IPM_OUTBOX_ENTRYID** est utilisée pour ouvrir le dossier Outbox uniquement pour les messages IPM. Si vous ouvrez la boîte d’envoi pour les messages IPC, utilisez plutôt l’identificateur d’entrée pour son dossier de réception. Les messages IPC entrants et sortants sont placés dans le dossier de réception. 
    
2. Appelez l’une des quatre méthodes **OpenEntry** pour ouvrir le dossier et retourner un pointeur d’interface que vous pouvez utiliser pour y accéder. Vous pouvez appeler l’une des méthodes suivantes pour ouvrir un dossier : 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   La méthode spécifique que vous choisissez dépend du dossier à ouvrir et des objets disponibles au moment de l’ouverture. Étant donné que la méthode **IMAPISession** peut ouvrir n’importe quel dossier pour n’importe quel magasin de messages dans le profil actuel, appelez cet **OpenEntry** lorsque vous ne savez rien sur le dossier à ouvrir. Si vous savez quel magasin de messages possède le dossier et que vous disposez d’un pointeur vers le magasin de messages, appelez **IMsgStore::OpenEntry**. 
    
   Par exemple, utilisez la méthode **IMsgStore** pour ouvrir un dossier de réception. Si vous avez un pointeur vers l’objet d’ouverture de session du fournisseur de magasin de messages, appelez **IMSLogon::OpenEntry**. Étant donné que ces appels sont directement transmis au fournisseur du magasin de messages plutôt qu’à MAPI, le traitement est plus rapide. Si le dossier que vous ouvrez est un sous-dossier d’un dossier que vous avez déjà ouvert, appelez la méthode **IMAPIContainer::OpenEntry** du dossier ouvert. La méthode **IMAPIContainer** ouvre uniquement les sous-dossiers d’un dossier actuellement ouvert et est la seule méthode garantie pour fonctionner avec des identificateurs d’entrée à court terme. 
    
3. Si vous souhaitez pouvoir apporter des modifications au dossier à ouvrir, spécifiez un niveau d’accès en définissant l’indicateur MAPI\_BEST\_ACCESS ou MAPI\_MODIFY dans l’appel **OpenEntry** . Ces indicateurs sont des suggestions au fournisseur du magasin de messages pour accorder le niveau d’accès le plus élevé, pour MAPI\_BEST\_ACCESS, ou un accès en lecture/écriture, pour MAPI\_MODIFY, lors de l’ouverture du dossier. 

   Étant donné que ces indicateurs ne sont que des suggestions, le dossier peut ou non être ouvert avec le niveau d’accès attendu. En récupérant la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), vous pouvez déterminer la plage d’opérations qui peuvent être effectuées sur le dossier ouvert. 
    
   Toutefois, étant donné que de nombreux fournisseurs de magasins de messages calculent la valeur de cette propriété à la demande plutôt que de la prendre en charge en tant que propriété de dossier ou en tant que colonne dans la table de leur hiérarchie, la récupération peut prendre du temps. Une autre stratégie consiste à tenter l’opération que vous devez effectuer et à retourner une erreur si nécessaire.
    
## <a name="see-also"></a>Voir aussi

- [Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

