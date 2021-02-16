---
title: Ouverture d’un dossier d’une banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: df7db013cb435484c721388abab51ab4ba43828f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436537"
---
# <a name="opening-a-message-store-folder"></a>Ouverture d’un dossier d’une banque de messages

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour pouvoir ouvrir un dossier, son identificateur d’entrée doit être disponible. Pour la plupart des dossiers, cela implique la récupération de leurs **propriétés PR_ENTRYID** propriétés. Pour les dossiers spéciaux, tels que certains des dossiers de sous-arbre IPM et d’autres dossiers racine, MAPI définit des propriétés d’identificateur d’entrée spéciales qui sont accessibles en appelant la méthode **IMAPIProp::GetProps** de la boutique de messages. Ces identificateurs d’entrée sont toujours à long terme et sont nommés comme suit : 
  
|**Folder**|**Propriété d’identificateur d’entrée**|
|:-----|:-----|
|Dossier bo�te d'envoi  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (classe de message IPM uniquement)  <br/> |
|dossier Éléments supprimés  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|dossier �l�ments envoy�s  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|Dossier racine IPM  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Dossier racine de r�sultats de recherche  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Dossier racine des affichages communs  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Dossier racine des affichages personnels  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Dossier racine contacts  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Dossier racine Brouillons  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Dossier racine du journal  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Dossier racine du calendrier  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Dossier racine Notes  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Dossier racine des tâches  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Avant d’essayer de récupérer l’un de ces identificateurs d’entrée spéciaux, récupérez la propriété **pr \_ VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) de la magasin de messages. **PR \_ VALID_FOLDER_MASK** est un masque de bits qui identifie lequel des identificateurs d’entrée spéciaux existe. Il existe un bit pour chacun des dossiers spéciaux. Si le bit est définie, il indique que le dossier correspondant est pris en charge et possède un identificateur d’entrée valide. Par exemple, si le dossier Éléments supprimés existe et qu’il possède un identificateur d’entrée valide, le bit IPM_WASTEBASKET_VALID FOLDER sera définie dans \_ **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Ouvrir le dossier dans lequel tous les messages entrants d’une classe particulière sont placés
  
1. Appelez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer son identificateur d’entrée, en paramétrage du paramètre  _lpszMessageClass_ pour qu’il pointe vers une chaîne de caractères identifiant la classe de message. Par exemple, si vous souhaitez ouvrir la boîte de réception de votre sous-arbre IPM, pointez  _lpszMessageClass_ vers IPM. Si vous souhaitez ouvrir le dossier de réception pour les messages IPC, définissez-le pour qu’il pointe vers IPC. 

   S’il n’existe aucun dossier de réception enregistré pour la classe de message, **GetReceiveFolder** choisit le dossier de réception dont la classe de message associée correspond au préfixe le plus long possible de la classe de message transmise. Pour plus d’informations, [voir Dossiers de réception MAPI.](mapi-receive-folders.md) 
   
   Notez que la **PR_IPM_OUTBOX_ENTRYID** est utilisée pour ouvrir le dossier Boîte d’envoi uniquement pour les messages IPM. Si vous ouvrent la boîte d’envoi pour les messages IPC, utilisez plutôt l’identificateur d’entrée pour son dossier de réception. Les messages IPC entrants et sortants sont placés dans le dossier de réception. 
    
2. Appelez l’une des quatre méthodes **OpenEntry** pour ouvrir le dossier et renvoyer un pointeur d’interface que vous pouvez utiliser pour y accéder. Vous pouvez appeler l’une des méthodes suivantes pour ouvrir un dossier : 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   La méthode spécifique que vous choisissez dépend du dossier à ouvrir et des objets disponibles à ce moment-là. Étant donné que la méthode **IMAPISession** peut ouvrir n’importe quel dossier pour n’importe quelle magasine de messages dans le profil actuel, appelez cet **OpenEntry** lorsque vous ne connaissez rien du dossier à ouvrir. Si vous connaissez la boutique de messages propriétaire du dossier et que vous avez un pointeur vers la boutique de messages, appelez **IMsgStore::OpenEntry**. 
    
   Par exemple, utilisez la **méthode IMsgStore** pour ouvrir un dossier de réception. Si vous avez un pointeur vers l’objet d’ouverture de conférence du fournisseur de magasins de messages, appelez **IMSLogon::OpenEntry**. Étant donné que ces appels sont directement envoyés au fournisseur de la boutique de messages plutôt que via MAPI, le traitement est plus rapide. Si le dossier que vous ouvrez est un sous-dossier d’un dossier que vous avez déjà ouvert, appelez la méthode **IMAPIContainer::OpenEntry** du dossier ouvert. La **méthode IMAPIContainer** ouvre uniquement les sous-dossiers d’un dossier actuellement ouvert et est la seule méthode qui fonctionne avec les identificateurs d’entrée à court terme. 
    
3. Si vous souhaitez être en mesure d’apporter des modifications au dossier à ouvrir, spécifiez un niveau d’accès en spécifiant l’indicateur MAPI BEST ACCESS ou MAPI MODIFY dans l’appel \_ \_ \_ **OpenEntry.** Ces indicateurs sont des suggestions au fournisseur de magasin de messages pour accorder le niveau d’accès le plus élevé, pour MAPI BEST ACCESS, ou accès en \_ \_ lecture/écriture, pour MAPI MODIFY, lors de l’ouverture du \_ dossier. 

   Étant donné que ces indicateurs ne sont que des suggestions, le dossier peut ou non être ouvert avec le niveau d’accès prévu. En récupérant la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), vous pouvez déterminer la plage d’opérations qui peut être effectuée sur le dossier ouvert. 
    
   Toutefois, étant donné que de nombreux fournisseurs de magasins de messages calculent la valeur de cette propriété à la demande plutôt que de la prendre en charge en tant que propriété de dossier ou en tant que colonne dans leur table hiérarchique, sa récupération peut prendre du temps. Une autre stratégie consiste à essayer l’opération que vous devez effectuer et à renvoyer une erreur si nécessaire.
    
## <a name="see-also"></a>Voir aussi

- [Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

