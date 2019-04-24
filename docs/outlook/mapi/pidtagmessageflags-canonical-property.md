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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325740"
---
# <a name="pidtagmessageflags-canonical-property"></a>Propriété canonique PidTagMessageFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de réindicateur des indicateurs qui indiquent l'origine et l'état actuel d'un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Identificateur :  <br/> |0x0E07  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une propriété de message non transmissible qui s'affiche aux extrémités de l'envoi et de la réception d'une transmission, avec des valeurs différentes en fonction de l'application client ou du fournisseur de magasin impliqué. Cette propriété est initialisée par le client ou le fournisseur de banque de messages lorsqu'un message est créé et enregistré pour la première fois, puis mis à jour périodiquement par le fournisseur de banque de messages, un fournisseur de transport et le spouleur MAPI lors du traitement du message et de son état. port. 
  
Cette propriété existe sur un message avant et après l'envoi, ainsi que sur toutes les copies du message reçu. Bien qu'il ne s'agisse pas d'une propriété Recipient, il est exposé différemment à chaque destinataire, selon qu'il a été lu ou modifié par ce destinataire. 
  
Un ou plusieurs des indicateurs suivants peuvent être définis pour cette propriété:
  
MSGFLAG_ASSOCIATED 
  
> Le message est un message associé à un dossier. Le client ou le fournisseur dispose d'un accès en lecture seule à cet indicateur. L'indicateur MSGFLAG_READ est ignoré pour les messages associés, qui ne conservent pas un État lecture/non lu. 
    
MSGFLAG_FROMME 
  
> L'utilisateur de messagerie expéditeur était l'utilisateur de messagerie qui reçoit le message. Le client ou le fournisseur dispose d'un accès en lecture/écriture à cet indicateur jusqu'au premier appel [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) et en lecture seule par la suite. Cet indicateur est destiné à être défini par le fournisseur de transport. 
    
MSGFLAG_HASATTACH 
  
> Le message comporte au moins une pièce jointe. Cet indicateur correspond à la propriété **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) du message. Le client dispose d'un accès en lecture seule à cet indicateur. 
    
MSGFLAG_NRN_PENDING 
  
> Un rapport non lu doit être envoyé pour le message. Le client ou le fournisseur dispose d'un accès en lecture seule à cet indicateur. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> Le message entrant est arrivé sur Internet. Elle provient de l'extérieur de l'organisation ou d'une source, la passerelle ne peut pas prendre en compte la confiance. Le client doit afficher un message approprié à l'utilisateur. Les fournisseurs de transport définissent cet indicateur; le client dispose d'un accès en lecture seule. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> Le message entrant est arrivé sur un lien externe autre que X. 400 ou Internet. Elle provient de l'extérieur de l'organisation ou d'une source, la passerelle ne peut pas prendre en compte la confiance. Le client doit afficher un message approprié à l'utilisateur. Les fournisseurs de transport définissent cet indicateur; le client dispose d'un accès en lecture seule. 
    
MSGFLAG_ORIGIN_X400 
  
> Le message entrant est arrivé sur une liaison X. 400. Elle provient de l'extérieur de l'organisation ou d'une source, la passerelle ne peut pas prendre en compte la confiance. Le client doit afficher un message approprié à l'utilisateur. Les fournisseurs de transport définissent cet indicateur; le client dispose d'un accès en lecture seule. 
    
MSGFLAG_READ 
  
> Le message est marqué comme lu. Cela peut se produire à tout moment en tant que résultat d'un appel à [IMessage:: SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md). Les clients peuvent également définir cet indicateur en appelant la méthode **IMAPIProp:: SetProps** d'un message avant la première sauvegarde du message. Cet indicateur est ignoré si l'indicateur **MSGFLAG_ASSOCIATED** est défini. 
    
MSGFLAG_RESEND 
  
> Le message inclut une demande pour une opération de renvoi avec un rapport de non-remise. Le client ou le fournisseur dispose d'un accès en lecture/écriture à cet indicateur jusqu'au premier appel [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) et en lecture seule par la suite. 
    
MSGFLAG_RN_PENDING 
  
> Un rapport de lecture doit être envoyé pour le message. Le client ou le fournisseur dispose d'un accès en lecture seule à cet indicateur. 
    
MSGFLAG_SUBMIT 
  
> Le message est marqué pour l'envoi à la suite d'un appel à [IMessage:: SubmitMessage](imessage-submitmessage.md). Les fournisseurs de banques de messages définissent cet indicateur; le client dispose d'un accès en lecture seule. 
    
MSGFLAG_UNMODIFIED 
  
> Le message sortant n'a pas été modifié depuis son premier enregistrement; le message entrant n'a pas été modifié depuis qu'il a été remis. 
    
MSGFLAG_UNSENT 
  
> Le message est toujours composé. Il est enregistré, mais n'a pas été envoyé. Le client ou le fournisseur dispose d'un accès en lecture/écriture à cet indicateur jusqu'au premier appel [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) et en lecture seule par la suite. Si un client ne définit pas cet indicateur lors de l'envoi du message, le fournisseur de banque de messages le définit lors de l'appel de **IMessage:: SubmitMessage** . En règle générale, cet indicateur est effacé après l'envoi du message. 
    
Un fournisseur de banque de messages ou un client peut vérifier l'état actuel du message à tout moment en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) pour lire les valeurs d'indicateur. Le client ou le fournisseur peut également appeler la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) pour modifier les indicateurs qui disposent actuellement d'un accès en lecture/écriture. 
  
Plusieurs indicateurs sont toujours en lecture seule. Certains sont en lecture/écriture jusqu'à ce que le premier appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) soit devenu en lecture seule en ce qui concerne **IMAPIProp:: SetProps** . L'un de ces éléments, MSGFLAG_READ, peut être modifié par la suite via [IMessage:: SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md). 
  
Les valeurs initiales de cette propriété sont généralement MSGFLAG_UNSENT et MSGFLAG_UNMODIFIED pour indiquer un message qui n'a pas encore été envoyé ou modifié. Lorsqu'un message est enregistré pour la deuxième fois, le fournisseur de banque de messages efface l'indicateur MSGFLAG_UNMODIFIED. Une autre valeur pouvant être définie par un fournisseur de banque de messages lors de l'enregistrement d'un message est l'indicateur MSGFLAG_HASATTACH, qui indique que le message comporte une ou plusieurs pièces jointes. La propriété **PR_HASATTACH** est calculée à partir de ce paramètre. 
  
Lorsqu'un client appelle la méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) pour envoyer le message, le fournisseur de banque de messages en fait une copie pour le spouleur MAPI et met à jour cette propriété en définissant l'indicateur MSGFLAG_SUBMIT. Le fournisseur de banque de messages définit également MSGFLAG_UNSENT s'il n'est pas encore défini. MSGFLAG_SUBMIT indique que **SubmitMessage** a été appelé, en commençant le processus d'envoi, et que le message est désormais en lecture seule sur le client. MSGFLAG_UNSENT indique que le spouleur MAPI gère le message. Si le processus d'envoi est annulé, le fournisseur de banque de messages réinitialise cet indicateur. 
  
Lorsque le message est remis à un fournisseur de transport en vue de sa remise, le fournisseur de transport définit l'indicateur MSGFLAG_FROMME si l'expéditeur a le même compte sur le serveur de messagerie que celui sur lequel le message a été reçu. Les fournisseurs de transport définissent MSGFLAG_FROMME pour un message entrant qui a été envoyé par l'utilisateur actuellement connecté. Un client peut utiliser cette valeur pour déterminer qu'il est plus approprié d'afficher les noms des destinataires dans la table des éléments envoyés que les noms des expéditeurs. Les messages qui ont été enregistrés pendant le processus de composition et qui n'ont pas encore été envoyés doivent également être affichés avec les noms des destinataires plutôt que les noms des expéditeurs. 
  
Pour un message entrant, un fournisseur de banque de messages efface l'indicateur MSGFLAG_READ pour réinitialiser son état de lecture. Un client peut définir ou effacer l'indicateur MSGFLAG_READ lorsqu'il est nécessaire de modifier l'état de lecture et de contrôler l'envoi de rapports lus et non lus en appelant la méthode [IMessage:: SetReadFlag](imessage-setreadflag.md) du message ou le [IMAPIFolder:: Méthode SetReadFlags](imapifolder-setreadflags.md) . La principale différence entre ces méthodes, à l'exception de l'objet qui les implémente, est que la méthode Folder peut affecter un, plusieurs ou tous les messages dans le dossier. La méthode message affecte un seul message. 
  
Un client doit également tester un message entrant pour les indicateurs MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET et MSGFLAG_ORIGIN_MISC_EXT. Ces indicateurs sont définis par le fournisseur de transport entrant et indiquent que le message est arrivé d'une source que la passerelle ne peut pas considérer comme approuvée. Cela signifie que le message provient soit de l'organisation, soit en interne, mais en provenance d'une station de travail inconnue de la passerelle. Dans tous les cas, l'identité de l'expéditeur peut ne pas être confirmée et il existe un risque d'introduire un virus informatique dans l'organisation. Le client doit afficher un message d'avertissement à l'utilisateur et proposer une option de suppression du message sans l'ouvrir. 
  
Les fournisseurs de banques de messages définissent l'indicateur MSGFLAG_UNMODIFIED pour les messages entrants. MSGFLAG_UNMODIFIED indique qu'un message n'a pas été modifié depuis sa remise. Un client ne peut pas effacer cette valeur après qu'elle a été définie par un fournisseur de banque de messages. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

