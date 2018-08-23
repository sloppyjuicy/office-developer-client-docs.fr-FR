---
title: L’envoi d’une réponse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4d8c995f5fbca322fca44cdcbb0de224af6b2fbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590287"
---
# <a name="sending-a-reply"></a>L’envoi d’une réponse

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Applications clientes prennent généralement en charge deux types de réponses : celui qui est envoyé uniquement à l’expéditeur du message d’origine et celui qui est envoyée à tous les autres destinataires inclus dans la liste des destinataires du message en plus de l’expéditeur d’origine. Ce deuxième type de réponse est communément appelé une réponse de que tous les messages.
  
Pour envoyer une réponse de des types, vous implémentez parmi les mêmes tâches que lorsque vous envoyez un message d’origine. Par exemple, vous ouvrez le dossier de message sortant, généralement la boîte d’envoi et de la banque de messages par défaut et appelez [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) méthode du dossier sortant pour créer la réponse. En outre, vous ouvrez le dossier qui conserve le message d’origine, généralement la boîte de réception. Pour plus d’informations sur l’ouverture des dossiers différents, consultez [ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md).
  
La principale différence entre la création d’une réponse et création d’un message d’origine est qu’avec une réponse, la plupart des propriétés est en fonction de soit copiée directement à partir des propriétés du message d’origine. Pièces jointes : propriété d’un message **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) — sont spécifiquement exclus. La liste de destinataires pour une réponse de tous les messages sont créé à partir de la liste du message d’origine avec le destinataire représenté par la propriété **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) et tous les destinataires en copie carbone invisible supprimés. La propriété **PR_RECEIVED_BY_SEARCH_KEY** représente l’utilisateur actuel. 
  
### <a name="to-send-a-reply"></a>Pour envoyer une réponse
  
1. Ouvrez la banque de messages par défaut. Pour plus d’informations, voir [l’ouverture de la banque de messages par défaut](opening-the-default-message-store.md).
    
2. Ouvrez le dossier boîte d’envoi. Pour plus d’informations, consultez [ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md).
    
3. Appelez la méthode de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la boîte d’envoi pour créer la réponse. 
    
4. Appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) du message d’origine pour copier les propriétés suivantes dans le message de réponse : 
    
   - **PR\_corps** ([PidTagBody](pidtagbody-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), en fonction de si vous prenez en charge le Format RTF.
    
   - **PR\_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), si la réponse est dirigés vers la liste entière des destinataires.
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. N’incluez pas les propriétés suivantes dans votre appel à **IMAPIProp::CopyTo**:
    
    |||
    |:-----|:-----|
    |**PR\_CLIENT\_envoi\_heure** <br/> |**PR\_MESSAGE\_remise\_heure** <br/> |
    |**PR\_MESSAGE\_télécharger\_heure** <br/> |**PR\_MESSAGE\_indicateurs** <br/> |
    |**PR\_expéditeur\_remise\_ REPORT\REQUESTED** <br/> |**PR\_reçu\_représentant** propriétés  <br/> |
    |**PR\_lire\_réception\_ENTRYID** <br/> |**PR\_lire\_réception\_requise** <br/> |
    |**PR\_reçu\_par** propriétés  <br/> |**PR\_réponse\_destinataire** propriétés  <br/> |
    |**PR\_rapport\_ENTRYID** <br/> |**PR\_expéditeur** propriétés  <br/> |
    |**PR\_SENT\_représentant** propriétés  <br/> |**PR\_SENTMAIL\_ENTRYID** <br/> |
    |**PR\_objet\_préfixe** <br/> | <br/> |
   
6. Ajouter un séparateur de texte à quelque propriété de corps de message vous prenez en charge : **PR_BODY**, **PR_HTM**L ou **PR_RTF_COMPRESSED**.
    
7. Appelez [ScCreateConversationIndex](sccreateconversationindex.md), en passant la valeur de la propriété **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) du message d’origine.
    
8. Définir un préfixe pour la réponse. Si vous utilisez la norme « RE : », concaténez ces caractères sur le début du **PR_NORMALIZED_SUBJECT** et définir **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) à la nouvelle chaîne. Ne définissez pas **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si vous utilisez un préfixe non standard, comme une chaîne de plus de trois caractères, stockez-la dans **PR_SUBJECT_PREFIX**. 
    
9. Définissez les propriétés **PR_SENT_REPRESENTING** sur les valeurs correspondantes dans les propriétés de **PR_RCVD_REPRESENTING** . 
    
10. Définissez chacune des entrées de **PR\_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) et **PR_REPLY\_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) à l’entrée identificateur et le nom complet d’un destinataire principal, un destinataire dont le type est MAPI_TO. Garder ces propriétés synchronisées. Autrement dit, **PR_REPLY_RECIPIENT\_entrées** **PR_REPLY_RECIPIENT_NAMES** doit contenir le même nombre d’entrées et une entrée à une position spécifique d’une des propriétés doit correspondre à une entrée à la même position dans l’autre propriété. 
    
11. Si la réponse est envoyée uniquement à l’expéditeur du message d’origine, créez une liste de destinataires d’entrée unique avec le destinataire représenté par la propriété **PR_SENT_REPRESENTING** du message d’origine. Pour plus d’informations sur la création d’une liste de destinataires, voir [Création d’une liste de destinataires](creating-a-recipient-list.md).
    
12. Si la réponse est une réponse tous, créez une liste de destinataires comme suit :
    
    1. Appelez la méthode de [IMessage::GetRecipientTable](imessage-getrecipienttable.md) du message d’origine pour accéder à la table des destinataires. 
        
    2. Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes dans le tableau. Déterminez si chaque ligne représente un destinataire principal ou copie carbone et doit rester dans la liste ou s’il représente un destinataire de copie carbone invisible ou de l’utilisateur et doit être supprimé de la liste. 
        
    3. Différencier les types de destinataires en consultant la colonne **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Cette colonne est fixée à MAPI_TO pour les destinataires principales, ni pour les destinataires en copie carbone et MAPI_BCC pour les destinataires en copie carbone invisible. 
        
    4. Comparez la colonne de **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) avec la propriété **PR_RECEIVED_BY_SEARCH_KEY** du message d’origine pour déterminer si la ligne représente l’utilisateur. 
        
    5. Supprimer les lignes à partir de la liste des destinataires en appelant [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire associée aux entrées correspondantes dans la structure de [SRowSet](srowset.md) de la table de destinataires. Définissez toutes les valeurs dans le tableau de valeurs de propriété à zéro, tous les membres **cValues** à zéro et tous les membres de chaque structure [SRow](srow.md) dans les **SRowSet** **lpProps** sur NULL. 
        
    6. Ajouter l’expéditeur à la liste des destinataires, tel que représenté par le message d’origine **PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) et **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) Propriétés. Vérifiez que l’expéditeur n’est pas dupliquée dans la liste.
        
    7. Appeler la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) du message de réponse au paramètre _ulFlags_ zéro, pour créer une nouvelle liste de destinataires pour la réponse ou transférer le message en fonction de la liste à partir du message d’origine. 
    
13. Appelez de la réponse [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour enregistrer le message ou [IMessage::SubmitMessage](imessage-submitmessage.md) pour enregistrer et envoyer. 
    
> [!NOTE]
> Avant d’appeler **IMessage::ModifyRecipients** pour enregistrer les modifications dans la liste des destinataires, vous pouvez permettre aux utilisateurs d’apporter des modifications par le biais du formulaire de message. Les utilisateurs peuvent ajouter à la liste ou supprimer des membres particulières. Permettre aux utilisateurs d’apporter des modifications à une liste de destinataires est une fonctionnalité de client facultatif. 
  

