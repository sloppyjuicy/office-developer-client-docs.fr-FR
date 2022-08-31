---
title: Propriété canonique PidTagMessageFlags
description: Décrit la propriété canonique PidTagMessageFlags, qui contient un masque de bits d’indicateurs qui indiquent l’origine et l’état actuel d’un message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageFlags
api_type:
- HeaderDef
ms.assetid: 7561112b-ca72-4c49-a8a0-cc1879a4e151
ms.openlocfilehash: ec0f1e0bc22bdfdaa67555db381f480ec7937fb7
ms.sourcegitcommit: 5839b9e3a6f0df249753f889c449a1620187461d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2022
ms.locfileid: "67485032"
---
# <a name="pidtagmessageflags-canonical-property"></a>Propriété canonique PidTagMessageFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits des indicateurs qui indiquent l’origine et l’état actuel d’un message. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Identificateur :  <br/> |0x0E07  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une propriété de message non transférable exposée aux extrémités d’envoi et de réception d’une transmission, avec des valeurs différentes en fonction de l’application cliente ou du fournisseur de magasin impliqué. Cette propriété est initialisée par le client ou le fournisseur du magasin de messages lorsqu’un message est créé et enregistré pour la première fois, puis mis à jour régulièrement par le fournisseur du magasin de messages, un fournisseur de transport et le spouleur MAPI au fur et à mesure que le message est traité et que son état change. 
  
Cette propriété existe sur un message avant et après l’envoi, ainsi que sur toutes les copies du message reçu. Bien qu’il ne s’agisse pas d’une propriété de destinataire, elle est exposée différemment à chaque destinataire selon qu’elle a été lue ou modifiée par ce destinataire. 
  
Un ou plusieurs des indicateurs suivants peuvent être définis pour cette propriété :
  
MSGFLAG_ASSOCIATED 
  
> Le message est un message associé à un dossier. Le client ou le fournisseur dispose d’un accès en lecture seule à cet indicateur. L’indicateur MSGFLAG_READ est ignoré pour les messages associés, qui ne conservent pas d’état de lecture/non lu. 
    
MSGFLAG_FROMME 
  
> L’utilisateur de messagerie qui a envoyé le message était l’utilisateur de messagerie qui recevait le message. Le client ou le fournisseur dispose d’un accès en lecture/écriture à cet indicateur jusqu’au premier appel [IMAPIProp::SaveChanges](imapiprop-savechanges.md) et en lecture seule par la suite. Cet indicateur est destiné à être défini par le fournisseur de transport. 
    
MSGFLAG_HASATTACH 
  
> Le message comporte au moins une pièce jointe. Cet indicateur correspond à la propriété **PR_HASATTACH** du message ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)). Le client dispose d’un accès en lecture seule à cet indicateur. 
    
MSGFLAG_NRN_PENDING 
  
> Un rapport non lu doit être envoyé pour le message. Le client ou le fournisseur dispose d’un accès en lecture seule à cet indicateur. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> Le message entrant est arrivé sur Internet. Il provient de l’extérieur de l’organisation ou d’une source que la passerelle ne peut pas considérer comme approuvée. Le client doit afficher un message approprié à l’utilisateur. Les fournisseurs de transport définissent cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> Le message entrant est arrivé via un lien externe autre que X.400 ou Internet. Il provient de l’extérieur de l’organisation ou d’une source que la passerelle ne peut pas considérer comme approuvée. Le client doit afficher un message approprié à l’utilisateur. Les fournisseurs de transport définissent cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_ORIGIN_X400 
  
> Le message entrant est arrivé via un lien X.400. Il provient de l’extérieur de l’organisation ou d’une source que la passerelle ne peut pas considérer comme approuvée. Le client doit afficher un message approprié à l’utilisateur. Les fournisseurs de transport définissent cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_ORIGIN_EXT_SEND

> Le message provient de l’extérieur de l’organisation. Le client doit afficher un message approprié à l’utilisateur. Les fournisseurs de transport définissent cet indicateur ; le client dispose d’un accès en lecture seule.

MSGFLAG_READ 
  
> Le message est marqué comme ayant été lu. Cela peut se produire à la suite d’un appel à tout moment à [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). Les clients peuvent également définir cet indicateur en appelant la méthode **IMAPIProp::SetProps** d’un message avant que le message n’ait été enregistré pour la première fois. Cet indicateur est ignoré si l’indicateur **MSGFLAG_ASSOCIATED** est défini. 
    
MSGFLAG_RESEND 
  
> Le message inclut une demande de renvoyer une opération avec un rapport non remis. Le client ou le fournisseur dispose d’un accès en lecture/écriture à cet indicateur jusqu’au premier appel [IMAPIProp::SaveChanges](imapiprop-savechanges.md) et en lecture seule par la suite. 
    
MSGFLAG_RN_PENDING 
  
> Un rapport de lecture doit être envoyé pour le message. Le client ou le fournisseur dispose d’un accès en lecture seule à cet indicateur. 
    
MSGFLAG_SUBMIT 
  
> Le message est marqué pour l’envoi à la suite d’un appel à [IMessage::SubmitMessage](imessage-submitmessage.md). Les fournisseurs du magasin de messages définissent cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_UNMODIFIED 
  
> Le message sortant n’a pas été modifié depuis sa première enregistrement ; le message entrant n’a pas été modifié depuis sa remise. 
    
MSGFLAG_UNSENT 
  
> Le message est toujours en cours de composition. Il est enregistré, mais n’a pas été envoyé. Le client ou le fournisseur dispose d’un accès en lecture/écriture à cet indicateur jusqu’au premier appel [IMAPIProp::SaveChanges](imapiprop-savechanges.md) et en lecture seule par la suite. Si un client ne définit pas cet indicateur au moment où le message est envoyé, le fournisseur du magasin de messages le définit quand **IMessage::SubmitMessage** est appelé. En règle générale, cet indicateur est effacé après l’envoi du message. 
    
Un client ou un fournisseur de magasin de messages peut vérifier l’état actuel du message à tout moment en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour lire les valeurs d’indicateur. Le client ou le fournisseur peut également appeler la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour modifier tous les indicateurs qui disposent actuellement d’un accès en lecture/écriture. 
  
Plusieurs indicateurs sont toujours en lecture seule. Certains sont en lecture/écriture jusqu’au premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , puis deviennent en lecture seule en ce qui concerne **IMAPIProp::SetProps** . L’un d’eux, MSGFLAG_READ, peut être modifié ultérieurement via [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). 
  
Les valeurs initiales de cette propriété sont généralement MSGFLAG_UNSENT et MSGFLAG_UNMODIFIED pour indiquer un message qui n’a pas encore été envoyé ou modifié. Lorsqu’un message est enregistré pour la deuxième fois, le fournisseur du magasin de messages efface l’indicateur MSGFLAG_UNMODIFIED. Une autre valeur qu’un fournisseur de magasin de messages peut définir lorsqu’un message est enregistré est l’indicateur MSGFLAG_HASATTACH, indiquant que le message comporte une ou plusieurs pièces jointes. La propriété **PR_HASATTACH** est calculée à partir de ce paramètre. 
  
Lorsqu’un client appelle la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer le message, le fournisseur du magasin de messages en effectue une copie pour le spouleur MAPI et met à jour cette propriété en définissant l’indicateur MSGFLAG_SUBMIT. Le fournisseur du magasin de messages définit également MSGFLAG_UNSENT s’il n’est pas encore défini. MSGFLAG_SUBMIT indique que **SubmitMessage** a été appelé, en commençant le processus d’envoi, et que le message est désormais en lecture seule au client. MSGFLAG_UNSENT indique que le spouleur MAPI gère le message. Si le processus d’envoi est annulé, le fournisseur du magasin de messages réinitialise cet indicateur. 
  
Lorsque le message est remis à un fournisseur de transport à des fins de remise, le fournisseur de transport définit l’indicateur de MSGFLAG_FROMME si l’expéditeur avait le même compte sur le serveur de messagerie que celui sur lequel le message a été reçu. Les fournisseurs de transport définissent MSGFLAG_FROMME pour un message entrant qui a été envoyé par l’utilisateur actuellement connecté. Un client peut utiliser cette valeur pour déterminer qu’il est plus approprié d’afficher les noms des destinataires dans la table des matières du dossier Éléments envoyés que les noms des expéditeurs. Les messages qui ont été enregistrés pendant le processus de composition et qui ne sont pas encore envoyés doivent également être affichés avec des noms de destinataires plutôt que des noms d’expéditeur. 
  
Pour un message entrant, un fournisseur de magasin de messages efface l’indicateur MSGFLAG_READ pour réinitialiser son état de lecture. Un client peut définir ou effacer l’indicateur de MSGFLAG_READ lorsqu’il est nécessaire de modifier l’état de lecture et de contrôler l’envoi de rapports en lecture et non lus, en appelant la méthode [IMessage::SetReadFlag](imessage-setreadflag.md) du message ou la méthode [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) de son dossier. La principale différence entre ces méthodes, autres que l’objet qui les implémente, est que la méthode de dossier peut affecter un, plusieurs ou tous les messages du dossier. La méthode de message affecte un seul message. 
  
Un client doit également tester un message entrant pour les indicateurs MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET, MSGFLAG_ORIGIN_MISC_EXT et MSGFLAG_ORIGIN_EXT_SEND. Ces indicateurs sont définis par le fournisseur de transport entrant et indiquent que le message est arrivé à partir d’une source que la passerelle ne peut pas considérer comme approuvée. Cela signifie que le message provient soit en dehors de l’organisation, soit en interne, mais à partir d’une station de travail inconnue de la passerelle. Dans tous les cas, l’identité de l’expéditeur peut ne pas être confirmée et il existe un risque d’introduction d’un virus informatique dans l’organisation. Le client doit afficher un message d’avertissement à l’utilisateur et offrir la possibilité de supprimer le message sans l’ouvrir. 
  
Les fournisseurs du magasin de messages définissent l’indicateur de MSGFLAG_UNMODIFIED pour les messages entrants. MSGFLAG_UNMODIFIED indique qu’un message n’a pas été modifié depuis la remise. Un client ne peut pas effacer cette valeur une fois qu’elle a été définie par un fournisseur de magasin de messages. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

