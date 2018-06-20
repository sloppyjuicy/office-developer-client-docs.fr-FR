---
title: Adresses SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9bc77e3226066dc88bbaf4f4efc324825add8919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787216"
---
# <a name="smtp-addresses"></a>Adresses SMTP

  
  
**S’applique à**: Outlook 
  
Le format des adresses de messagerie SMTP est défini dans RFC 822. Composants MAPI doivent gérer n’importe quelle adresse conforme à ce standard. Toutefois, il existe un formulaire particulier d’adresse RFC 822 mieux encode adresses MAPI :
  
 _nom d’affichage_ **\<** _- adresse de messagerie_**\>**
  
Les crochets sont inclus comme des caractères littéraux. Les espaces sont courants dans les noms d’affichage ; ils ne doivent pas mis entre guillemets. Une adresse peut ressembler à celui-ci, qui appartient à un des co-auteurs de RFC 1521 :
  
Nathaniel Borenstein \<nsb@bellcore.com\>
  
Si le nom d’affichage contienne des caractères qui ont une signification spéciale dans les adresses SMTP, tel que \< ou @, le nom de la totalité de l’affichage doit être placée entre guillemets doubles. Dans les messages sortants, si l’affichage de la longueur totale de l’adresse de messagerie plu nom dépasse 255 caractères, le nom complet doit être supprimé.
  
Les composants d’une adresse SMTP sont mappées à des propriétés MAPI, comme suit :
  
|**Composant d’adresse SMTP**|**Propriété MAPI**|
|:-----|:-----|
| _nom d’affichage_ pour tous les destinataires  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _nom d’affichage_ du champ  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _nom d’affichage_ pour le champ de l’expéditeur  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _adresse de messagerie_ <br/> |**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implicites, toujours « SMTP »  <br/> |**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
S’il n’existe aucun nom d’affichage pour une adresse sur le courrier entrant, l’adresse de messagerie entière doit être utilisé à la place. Le type d’adresse est toujours SMTP.
  
Propriétés de destinataire proviennent de la table des destinataires du message MAPI ; propriétés de l’expéditeur sont prises dans le message lui-même.
  

