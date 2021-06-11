---
title: Adresses SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419624"
---
# <a name="smtp-addresses"></a>Adresses SMTP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le format des adresses de messagerie SMTP est défini dans RFC 822. Les composants MAPI doivent gérer n’importe quelle adresse conforme à cette norme. Toutefois, il existe une forme particulière d’adresse RFC 822 qui code le mieux les adresses MAPI :
  
 _display-name_ **\<** _email-address_**\>**
  
Les crochets sont inclus en tant que littéraux. Les espaces vides sont courants dans les noms d’affichage ; ils n’ont pas besoin d’être entre eux. Une adresse type peut ressembler à celle-ci, qui appartient à l’un des co-auteurs de la RFC 1521 :
  
Nsb@bellcore.com \<\>
  
Si le nom complet contient des caractères qui ont une signification spéciale dans les adresses SMTP, telles que @, le nom complet doit être entre \< guillemets doubles. Sur le courrier sortant, si la longueur totale de l’adresse e-mail et du nom complet dépasse 255 caractères, le nom complet doit être supprimé.
  
Les composants d’une adresse SMTP sont mappés dans les propriétés MAPI comme suit :
  
|**Composant d’adresse SMTP**|**Propriété MAPI**|
|:-----|:-----|
| _nom complet de_ tous les destinataires  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _nom complet du_ champ De  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _nom complet du_ champ Expéditeur  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _email-address_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implicite, toujours « SMTP »  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
S’il n’existe pas de nom complet pour une adresse sur le courrier entrant, l’adresse e-mail entière doit être utilisée à la place. Le type d’adresse est toujours SMTP.
  
Les propriétés du destinataire sont tirées de la table des destinataires du message MAPI . les propriétés de l’expéditeur sont tirées du message lui-même.
  

