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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325740"
---
# <a name="pidtagmessageflags-canonical-property"></a>Propriété canonique PidTagMessageFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs qui indiquent l’origine et l’état actuel d’un message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Identificateur :  <br/> |0x0E07  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une propriété de message nontransmitable exposée aux extrémités d’envoi et de réception d’une transmission, avec des valeurs différentes en fonction de l’application cliente ou du fournisseur de magasins impliqué. Cette propriété est initialisée par le fournisseur de client ou de magasin de messages lorsqu’un message est créé et enregistré pour la première fois, puis mis à jour régulièrement par le fournisseur de la boutique de messages, un fournisseur de transport et lepooler MAPI à mesure que le message est traitée et que son état change. 
  
Cette propriété existe sur un message avant et après l’envoi et sur toutes les copies du message reçu. Bien qu’il ne s’agit pas d’une propriété de destinataire, elle est exposée différemment à chaque destinataire selon qu’elle a été lue ou modifiée par ce destinataire. 
  
Un ou plusieurs des indicateurs suivants peuvent être définies pour cette propriété :
  
MSGFLAG_ASSOCIATED 
  
> Le message est un message associé d’un dossier. Le client ou le fournisseur dispose d’un accès en lecture seule à cet indicateur. L MSGFLAG_READ est ignoré pour les messages associés, qui ne conservent pas un état de lecture/non lu. 
    
MSGFLAG_FROMME 
  
> L’utilisateur de messagerie qui envoie le message était l’utilisateur de messagerie qui reçoit le message. Le client ou le fournisseur dispose d’un accès en lecture/écriture à cet indicateur jusqu’au premier appel [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) puis en lecture seule par la suite. Cet indicateur est destiné à être définie par le fournisseur de transport. 
    
MSGFLAG_HASATTACH 
  
> Le message a au moins une pièce jointe. Cet indicateur correspond à la propriété **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)). Le client dispose d’un accès en lecture seule à cet indicateur. 
    
MSGFLAG_NRN_PENDING 
  
> Un rapport non lu doit être envoyé pour le message. Le client ou le fournisseur dispose d’un accès en lecture seule à cet indicateur. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> Le message entrant est arrivé sur Internet. Elle provient de l’extérieur de l’organisation ou d’une source que la passerelle ne peut pas considérer comme fiable. Le client doit afficher un message approprié à l’utilisateur. Les fournisseurs de transport définissent cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> Le message entrant est arrivé sur un lien externe autre que X.400 ou Internet. Elle provient de l’extérieur de l’organisation ou d’une source que la passerelle ne peut pas considérer comme fiable. Le client doit afficher un message approprié à l’utilisateur. Les fournisseurs de transport définissent cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_ORIGIN_X400 
  
> Le message entrant est arrivé sur un lien X.400. Elle provient de l’extérieur de l’organisation ou d’une source que la passerelle ne peut pas considérer comme fiable. Le client doit afficher un message approprié à l’utilisateur. Les fournisseurs de transport définissent cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_READ 
  
> Le message est marqué comme ayant été lu. Cela peut se produire à la suite d’un appel à tout moment à [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). Les clients peuvent également définir cet indicateur en appelant la méthode **IMAPIProp::SetProps** d’un message avant que le message ait été enregistré pour la première fois. Cet indicateur est ignoré si **l’MSGFLAG_ASSOCIATED** est définie. 
    
MSGFLAG_RESEND 
  
> Le message inclut une demande d’opération de renvoyer avec un rapport nondelivery. Le client ou le fournisseur dispose d’un accès en lecture/écriture à cet indicateur jusqu’au premier appel [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) puis en lecture seule par la suite. 
    
MSGFLAG_RN_PENDING 
  
> Un rapport de lecture doit être envoyé pour le message. Le client ou le fournisseur dispose d’un accès en lecture seule à cet indicateur. 
    
MSGFLAG_SUBMIT 
  
> Le message est marqué pour l’envoi à la suite d’un appel à [IMessage::SubmitMessage](imessage-submitmessage.md). Les fournisseurs de magasins de messages définissent cet indicateur ; le client dispose d’un accès en lecture seule. 
    
MSGFLAG_UNMODIFIED 
  
> Le message sortant n’a pas été modifié depuis son premier enregistré . le message entrant n’a pas été modifié depuis sa livraison. 
    
MSGFLAG_UNSENT 
  
> Le message est toujours en cours de composition. Il est enregistré, mais n’a pas été envoyé. Le client ou le fournisseur dispose d’un accès en lecture/écriture à cet indicateur jusqu’au premier appel [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) puis en lecture seule par la suite. Si un client ne définit pas cet indicateur au moment de l’envoi du message, le fournisseur de la boutique de messages le définit lors de l’appel **d’IMessage::SubmitMessage.** En règle générale, cet indicateur est effacé après l’envoi du message. 
    
Un client ou un fournisseur de magasins de messages peut vérifier l’état actuel du message à tout moment en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour lire les valeurs d’indicateur. Le client ou le fournisseur peut également appeler la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour modifier les indicateurs qui disposent actuellement d’un accès en lecture/écriture. 
  
Plusieurs indicateurs sont toujours en lecture seule. Certains sont en lecture/écriture jusqu’au premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) et deviennent ensuite en lecture seule dans la mesure où **IMAPIProp::SetProps** est concerné. L’un MSGFLAG_READ, peut être modifié ultérieurement via [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). 
  
Les valeurs initiales de cette propriété sont généralement MSGFLAG_UNSENT et MSGFLAG_UNMODIFIED pour indiquer un message qui n’a pas encore été envoyé ou modifié. Lorsqu’un message est enregistré pour la deuxième fois, le fournisseur de la boutique de messages MSGFLAG_UNMODIFIED’indicateur. Une autre valeur qu’un fournisseur de magasins de messages peut définir lorsqu’un message est enregistré est l’indicateur MSGFLAG_HASATTACH, indiquant que le message a une ou plusieurs pièces jointes. La **PR_HASATTACH** est calculée à partir de ce paramètre. 
  
Lorsqu’un client appelle la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer le message, le fournisseur de magasin de messages en fait une copie pour lepooler MAPI et met à jour cette propriété en MSGFLAG_SUBMIT indicateur. Le fournisseur de magasins de messages définit également MSGFLAG_UNSENT si elle n’est pas encore définie. MSGFLAG_SUBMIT indique que **SubmitMessage** a été appelé, en commençant le processus d’envoi, et que le message est désormais en lecture seule pour le client. MSGFLAG_UNSENT indique que lepooler MAPI gère le message. Si le processus d’envoi est annulé, le fournisseur de la boutique de messages réinitialise cet indicateur. 
  
Lorsque le message est remis à un fournisseur de transport pour remise, le fournisseur de transport définit l’indicateur MSGFLAG_FROMME si l’expéditeur avait le même compte sur le serveur de messagerie que le message reçu. Les fournisseurs de transport définissent MSGFLAG_FROMME pour un message entrant envoyé par l’utilisateur actuellement connecté. Un client peut utiliser cette valeur pour déterminer qu’il est plus approprié d’afficher les noms des destinataires dans la table des matières du dossier Éléments envoyés que les noms des expéditeurs. Les messages qui ont été enregistrés pendant le processus de composition et qui n’ont pas encore été envoyés doivent également être affichés avec des noms de destinataires plutôt que des noms d’expéditeur. 
  
Pour un message entrant, un fournisseur de magasins de messages MSGFLAG_READ l’indicateur pour réinitialiser son état de lecture. Un client peut définir ou effacer l’indicateur MSGFLAG_READ lorsqu’il est nécessaire de modifier l’état de lecture et de contrôler l’envoi de rapports de lecture et non lus, en appelant la méthode [IMessage::SetReadFlag](imessage-setreadflag.md) du message ou la méthode [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) de son dossier. La principale différence entre ces méthodes, autre que l’objet qui les implémente, est que la méthode de dossier peut affecter un, plusieurs ou tous les messages du dossier. La méthode de message affecte un seul message. 
  
Un client doit également tester un message entrant pour les indicateurs MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET et MSGFLAG_ORIGIN_MISC_EXT réception. Ces indicateurs sont définies par le fournisseur de transport entrant et indiquent que le message est arrivé d’une source que la passerelle ne peut pas considérer comme fiable. Cela signifie que le message provient soit de l’extérieur de l’organisation, soit en interne, mais d’une station de travail inconnue de la passerelle. Dans tous les cas, l’identité de l’expéditeur peut ne pas être confirmée et il existe un risque d’introduire un virus informatique dans l’organisation. Le client doit afficher un message d’avertissement à l’utilisateur et offrir la possibilité de le supprimer sans l’ouvrir. 
  
Les fournisseurs de magasins de messages définissent l MSGFLAG_UNMODIFIED pour les messages entrants. MSGFLAG_UNMODIFIED indique qu’un message n’a pas été modifié depuis la remise. Un client ne peut pas effacer cette valeur une fois qu’elle a été définie par un fournisseur de magasins de messages. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

