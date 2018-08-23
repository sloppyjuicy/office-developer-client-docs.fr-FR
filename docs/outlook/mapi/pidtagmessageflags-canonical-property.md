---
title: Propriété canonique PidTagMessageFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageFlags
api_type:
- HeaderDef
ms.assetid: 7561112b-ca72-4c49-a8a0-cc1879a4e151
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8082b0b6d47a16a79f5e426375e20b17d22298d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586619"
---
# <a name="pidtagmessageflags-canonical-property"></a>Propriété canonique PidTagMessageFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un masque binaire composé des indicateurs qui influencent l’origine et l’état actuel d’un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Identificateur :  <br/> |0x0E07  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une propriété de message nontransmittable exposée à l’envoi et la réception des extrémités d’une transmission, avec des valeurs différentes selon le fournisseur client application ou banque impliqué. Cette propriété est initialisée par le fournisseur de banque client ou d’un message lorsqu’un message est créé et enregistré pour la première fois et puis mis à jour régulièrement par le fournisseur de banque de message, un fournisseur de transport et le spouleur MAPI comme le message est traité et son état modifications apportées. 
  
Cette propriété existe sur un message à la fois avant et après la présentation et sur toutes les copies du message reçu. Bien qu’il n’est pas une propriété de destinataire, il est exposé différemment pour chaque destinataire en fonction de si elle a été lire ou modifié par ce destinataire. 
  
Un ou plusieurs des indicateurs suivants peuvent être définie pour cette propriété :
  
MSGFLAG_ASSOCIATED 
  
> Le message est un message d’un dossier associé. Le client ou le fournisseur dispose d’un accès en lecture seule pour cet indicateur. L’indicateur MSGFLAG_READ est ignorée pour les messages associés, qui ne conservent pas d’un état en lecture/non lus. 
    
MSGFLAG_FROMME 
  
> L’utilisateur de messagerie envoi a été l’utilisateur de messagerie reçoit le message. Le client ou le fournisseur a accès en lecture/écriture à cet indicateur jusqu'à ce que le premier appel [IMAPIProp::SaveChanges](imapiprop-savechanges.md) et en lecture seule par la suite. Cet indicateur est destiné à être définie par le fournisseur de transport. 
    
MSGFLAG_HASATTACH 
  
> Le message comporte au moins une pièce jointe. Cet indicateur correspond à la propriété **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) du message. Le client dispose d’un accès en lecture seule pour cet indicateur. 
    
MSGFLAG_NRN_PENDING 
  
> Un rapport nonread doit être envoyé pour le message. Le client ou le fournisseur dispose d’un accès en lecture seule pour cet indicateur. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> Le message entrant est arrivé sur Internet. Elle a été créée à l’extérieur de l’organisation ou d’une source de que la passerelle ne peut pas prendre en compte approuvé. Le client doit afficher un message approprié pour l’utilisateur. Fournisseurs de transport de définir cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> Le message entrant est arrivé sur un lien externe autre que X.400 ou Internet. Elle a été créée à l’extérieur de l’organisation ou d’une source de que la passerelle ne peut pas prendre en compte approuvé. Le client doit afficher un message approprié pour l’utilisateur. Fournisseurs de transport de définir cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_ORIGIN_X400 
  
> Le message entrant est arrivé sur un lien X.400. Elle a été créée à l’extérieur de l’organisation ou d’une source de que la passerelle ne peut pas prendre en compte approuvé. Le client doit afficher un message approprié pour l’utilisateur. Fournisseurs de transport de définir cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_READ 
  
> Le message est marqué comme ayant été lu. Cela peut se produire à la suite d’un appel à tout moment à [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). Les clients peuvent également définir cet indicateur en appelant la méthode de **IMAPIProp::SetProps** d’un message avant que le message a été enregistré pour la première fois. Cet indicateur est ignoré si l’indicateur **MSGFLAG_ASSOCIATED** est défini. 
    
MSGFLAG_RESEND 
  
> Le message comporte une demande pour une opération de renvoyer un rapport de non-remise. Le client ou le fournisseur a accès en lecture/écriture à cet indicateur jusqu'à ce que le premier appel [IMAPIProp::SaveChanges](imapiprop-savechanges.md) et en lecture seule par la suite. 
    
MSGFLAG_RN_PENDING 
  
> Un rapport de lecture doit être envoyé pour le message. Le client ou le fournisseur dispose d’un accès en lecture seule pour cet indicateur. 
    
MSGFLAG_SUBMIT 
  
> Le message est marqué pour l’envoi à la suite d’un appel à [IMessage::SubmitMessage](imessage-submitmessage.md). Fournisseurs de banque de messages de définir cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_UNMODIFIED 
  
> Le message sortant n’a pas été modifié depuis la première fois qu’il a été enregistré ; le message entrant n’a pas été modifié depuis qu’il a été remis. 
    
MSGFLAG_UNSENT 
  
> Le message est toujours en cours composé. Il est enregistré, mais n’a pas été envoyé. Le client ou le fournisseur a accès en lecture/écriture à cet indicateur jusqu'à ce que le premier appel [IMAPIProp::SaveChanges](imapiprop-savechanges.md) et en lecture seule par la suite. Si un client ne définit pas cet indicateur au moment où que le message est envoyé, le fournisseur de banque de messages définit lorsque **IMessage::SubmitMessage** est appelée. En règle générale, cet indicateur est désactivé une fois que le message est envoyé. 
    
Un fournisseur de magasin client ou d’un message peut vérifier l’état actuel du message à tout moment en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour lire les valeurs d’indicateur. Le client ou le fournisseur peut également appeler la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour modifier les indicateurs qui possèdent un accès en lecture/écriture. 
  
Plusieurs des indicateurs sont toujours en lecture seule. Certains sont en lecture/écriture jusqu'à ce que le premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) et ensuite en lecture seule comme **IMAPIProp::SetProps** est concerné. Une de ces, MSGFLAG_READ, peut être modifiée ultérieurement via [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). 
  
Les valeurs initiales de cette propriété sont généralement MSGFLAG_UNSENT et MSGFLAG_UNMODIFIED pour indiquer que le message n’est pas encore été envoyé ou modifié. Lorsqu’un message est enregistré pour la deuxième fois, le fournisseur de banque de messages efface l’indicateur MSGFLAG_UNMODIFIED. Une autre valeur pour paramétrer un fournisseur de magasin de message lorsqu’un message est enregistré est l’indicateur MSGFLAG_HASATTACH, indiquant que le message comporte une ou plusieurs pièces jointes. La propriété **PR_HASATTACH** est calculée à partir de ce paramètre. 
  
Lorsqu’un client appelle la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer le message, le fournisseur de banque de messages crée une copie de celle-ci pour le spouleur MAPI et met à jour de cette propriété en définissant l’indicateur MSGFLAG_SUBMIT. Le fournisseur de banque de messages définit également MSGFLAG_UNSENT si elle n’est pas encore défini. MSGFLAG_SUBMIT indique que **SubmitMessage** a été appelée, démarrer le processus d’envoi, et que le message est maintenant en lecture seule pour le client. MSGFLAG_UNSENT indique que le spouleur MAPI gère le message. Si le processus d’envoi est annulé, le fournisseur de banque de messages réinitialise cet indicateur. 
  
Lorsque le message est affecté à un fournisseur de transport pour la livraison, le fournisseur de transport définit l’indicateur MSGFLAG_FROMME si l’expéditeur a le même compte sur le serveur de messagerie, le message a été reçu sur le. Fournisseurs de transport définir MSGFLAG_FROMME pour un message entrant a été envoyé par l’utilisateur actuellement connecté. Un client peut utiliser cette valeur pour déterminer qu’il est plus approprié afficher les noms des destinataires dans le tableau contenu du dossier éléments envoyés de noms de l’expéditeur. Les messages qui ont été enregistrées au cours du processus de composition et n’est pas encore envoyés doivent également s’afficher avec les noms des destinataires plutôt que des noms de l’expéditeur. 
  
Un message entrant, un fournisseur de magasin de message efface l’indicateur MSGFLAG_READ pour rétablir son état de lecture. Un client peut définir ou effacer l’indicateur MSGFLAG_READ lorsqu’il est nécessaire de modifier l’état de lecture et de contrôler l’envoi de rapports de lecture et nonread, en appelant la méthode [IMessage::SetReadFlag](imessage-setreadflag.md) du message ou de son dossier [IMAPIFolder :: SetReadFlags](imapifolder-setreadflags.md) méthode. La différence principale entre ces méthodes, autre que l’objet de les implémenter, est que la méthode du dossier peut affecter un, plusieurs ou tous les messages dans le dossier. La méthode message concerne un seul message. 
  
Un client doit également tester un message entrant pour les indicateurs MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET et MSGFLAG_ORIGIN_MISC_EXT. Ces indicateurs sont définis par le fournisseur de transport entrant et indiquent que le message est arrivé à partir d’une source de la passerelle ne peut pas prendre en compte approuvé. Cela signifie que le message provient de l’extérieur de l’organisation, ou en interne, mais à partir d’une station de travail ne pas connue vers la passerelle. Dans tous les cas, l’identité de l’expéditeur ne peut pas être confirmée, et il existe un risque d’introduction d’un virus dans l’organisation. Le client doit afficher un message d’avertissement à l’utilisateur et offre une possibilité de supprimer le message sans l’ouvrir. 
  
Fournisseurs de magasins message définir l’indicateur MSGFLAG_UNMODIFIED pour les messages entrants. MSGFLAG_UNMODIFIED indique qu’un message n’a pas été modifié depuis la remise. Un client ne peut pas effacer cette valeur après que elle a été définie par un fournisseur de magasin de message. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

