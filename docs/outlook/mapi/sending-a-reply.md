---
title: Envoi d’une réponse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: 'Les applications clientes peuvent prendre en charge deux types de réponses : une qui est envoyée uniquement à l’expéditeur du message d’origine et une autre qui est envoyée à tous les autres destinataires.'
ms.openlocfilehash: 210e3dc129d3a0b298a971a158ca8e6a6ec8848d
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455915"
---
# <a name="sending-a-reply"></a>Envoi d’une réponse

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes prend généralement en charge deux types de réponses : une qui est envoyée uniquement à l’expéditeur du message d’origine et une autre qui est envoyée à tous les autres destinataires inclus dans la liste des destinataires du message d’origine en plus de l’expéditeur. Ce deuxième type de réponse est communément appelé « réponse à tous les messages ».
  
Pour envoyer une réponse de l’un ou l’autre type, vous implémentez certaines des mêmes tâches que lorsque vous envoyez un message d’origine. Par exemple, vous ouvrez la boîte aux lettres par défaut et le dossier des messages sortants, généralement la boîte d’envoi, et appelez la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) du dossier sortant pour créer la réponse. En outre, vous ouvrez le dossier qui contient le message d’origine, généralement la boîte de réception. Pour plus d’informations sur l’ouverture de différents dossiers, voir [Opening a Message Store Folder](opening-a-message-store-folder.md).
  
La principale différence entre la création d’une réponse et la création d’un message d’origine est qu’avec une réponse, la plupart des propriétés sont basées sur ou copiées directement à partir des propriétés du message d’origine. Les pièces jointes, la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) d’un message, sont spécifiquement exclues. La liste des destinataires d’une réponse à tous les messages est créée à partir de la liste du message d’origine avec le destinataire représenté par la propriété **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) et tous les destinataires en copie carbone non voyante supprimés. La **PR_RECEIVED_BY_SEARCH_KEY** représente l’utilisateur actuel. 
  
### <a name="to-send-a-reply"></a>Pour envoyer une réponse
  
1. Ouvrez la boutique de messages par défaut. Pour plus d’informations, voir [Ouverture de la boutique de messages par défaut](opening-the-default-message-store.md).
    
2. Ouvrez le dossier Boîte d’envoi. Pour plus d’informations, voir [Ouverture d’un dossier de la boutique de messages](opening-a-message-store-folder.md).
    
3. Appelez la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la boîte d’envoi pour créer la réponse. 
    
4. Appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) du message d’origine pour copier les propriétés suivantes dans le message de réponse : 
    
   - **PR\_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), selon que vous prise en charge ou non le format de texte enrichi.
    
   - **PR\_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), si la réponse est aller à l’intégralité de la liste des destinataires.
    
   - **PR\_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. N’incluez pas les propriétés suivantes dans votre appel **à IMAPIProp::CopyTo** :
    
    |Property |... |
    |:-----|:-----|
    |**PRCLIENTSUBMITTIME\_\_\_** <br/> |**PRMESSAGEDELIVERYTIME\_\_\_** <br/> |
    |**PRMESSAGEDOWNLOADTIME\_\_\_** <br/> |**PRMESSAGEFLAGS\_\_** <br/> |
    |**RAPPORT PRORIGINATORDELIVERY\_\_\_\REQUESTED** <br/> |**PR\_ Propriétés RCVDREPRESENTING\_**  <br/> |
    |**PRREADRECEIPTENTRYID\_\_\_** <br/> |**PRREADRECEIPTREQUESTED\_\_\_** <br/> |
    |**PR\_ Propriétés RECEIVEDBY\_**  <br/> |**PR\_ Propriétés REPLYRECIPIENT\_**  <br/> |
    |**PRREPORTENTRYID\_\_** <br/> |**PR\_ Propriétés SENDER**  <br/> |
    |**PR\_ Propriétés SENTREPRESENTING\_**  <br/> |**PRSENTMAILENTRYID\_\_** <br/> |
    |**PRSUBJECTPREFIX\_\_** <br/> | <br/> |
   
6. Ajoutez du texte de séparation à la propriété de corps de message que **vous prendrez en charge ( PR_BODY**, **PR_HTM** L ou **PR_RTF_COMPRESSED**.
    
7. Appelez [ScCreateConversationIndex](sccreateconversationindex.md), en passant la valeur de la propriété **PR_CONVERSATION_INDEX (**[PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) du message d’origine.
    
8. Définissez un préfixe pour la réponse. Si vous utilisez la norme « RE: », concaténer ces caractères au début de **PR_NORMALIZED_SUBJECT** et définissez **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) sur cette nouvelle chaîne. Ne définissez **pas PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si vous utilisez un préfixe nonstandard, tel qu’une chaîne de plus de trois caractères, stockez-le **dans PR_SUBJECT_PREFIX**. 
    
9. Définissez **les PR_SENT_REPRESENTING** sur les valeurs correspondantes dans la **PR_RCVD_REPRESENTING** propriétés. 
    
10. Définissez chacune des entrées dans **pr\_ REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) et **PR_REPLY\_ RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) sur l’identificateur d’entrée et le nom complet d’un destinataire principal , un destinataire dont le type est MAPI_TO. Maintenez ces propriétés synchronisées. Autrement dit, **PR_REPLY_RECIPIENT\_ ENTRIES** et **PR_REPLY_RECIPIENT_NAMES** doivent contenir le même nombre d’entrées, et une entrée à une position particulière dans l’une des propriétés doit correspondre à une entrée à la même position dans l’autre propriété. 
    
11. Si la réponse est envoyée uniquement à l’expéditeur du message d’origine, créez une liste de destinataires d’entrée unique avec le destinataire représenté par la propriété **PR_SENT_REPRESENTING d’origine** . Pour plus d’informations sur la création d’une liste de destinataires, voir [Création d’une liste de destinataires](creating-a-recipient-list.md).
    
12. Si la réponse est une réponse à tous, créez une liste de destinataires comme suit :
    
    1. Appelez la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) du message d’origine pour accéder à sa table des destinataires. 
        
    2. [Appelez HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes du tableau. Déterminez si chaque ligne représente un destinataire de copie principale ou carbone et doit rester dans la liste ou si elle représente un destinataire de copie carbone non voyante ou l’utilisateur et doit être supprimée de la liste. 
        
    3. Différencier les types de destinataires en regardant la **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Cette colonne sera définie sur MAPI_TO pour les destinataires principaux, MAPI_CC pour les destinataires en copie carbone et MAPI_BCC pour les destinataires de copie carbone non voyante. 
        
    4. Comparez **la PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) à la propriété **PR_RECEIVED_BY_SEARCH_KEY** du message d’origine pour déterminer si la ligne représente l’utilisateur. 
        
    5. Supprimez les lignes indésirables de la liste des destinataires en appelant [MAPIFreeBuffer](mapifreebuffer.md) pour libérer la mémoire associée aux entrées correspondantes dans la structure [SRowSet](srowset.md) de la table des destinataires. Définissez toutes les valeurs du tableau de valeurs de propriété sur zéro, tous les membres **cValues** sur zéro et tous les membres **lpProps** dans chaque structure [SRow](srow.md) dans **le SRowSet** sur NULL. 
        
    6. Ajoutez l’expéditeur à la liste des destinataires, tel que représenté par les propriétés **PR\_ SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) et **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) du message d’origine. Vérifiez que l’expéditeur n’est pas dupliqué dans la liste.
        
    7. Appelez la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) du message de réponse, en fixant le paramètre  _ulFlags_ sur zéro, pour créer une nouvelle liste de destinataires pour la réponse ou le message transmis en fonction de la liste du message d’origine. 
    
13. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la réponse pour enregistrer le message ou [IMessage::SubmitMessage](imessage-submitmessage.md) pour l’enregistrer et l’envoyer. 
    
> [!NOTE]
> Avant **d’appeler IMessage::ModifyRecipients** pour stocker les modifications dans la liste des destinataires, vous pouvez autoriser les utilisateurs à apporter des modifications via le formulaire de message. Les utilisateurs peuvent ajouter à la liste ou supprimer des membres particuliers. Autoriser les utilisateurs à apporter des modifications à une liste de destinataires est une fonctionnalité cliente facultative. 
  

