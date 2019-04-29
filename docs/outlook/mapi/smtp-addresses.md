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
  
Le format des adresses de messagerie SMTP est défini dans la norme RFC 822. Les composants MAPI doivent gérer toute adresse conforme à cette norme. Toutefois, il existe une forme particulière d'adresse RFC 822 qui code le mieux pour les adresses MAPI:
  
 _nom d'affichage_ **\<** _adresse de messagerie_**\>**
  
Les chevrons sont inclus sous forme de littéraux. Les espaces sont courants dans les noms d'affichage; ils n'ont pas besoin d'être cités. Une adresse classique peut ressembler à celle-ci, qui appartient à l'un des coauteurs de la norme RFC 1521:
  
Nathaniel Borenstein \<NSB@bellcore.com\>
  
Si le nom d'affichage contient des caractères qui ont une signification particulière dans des adresses \< SMTP, par exemple, ou @, l'intégralité du nom complet doit être placée entre guillemets doubles. Pour le courrier sortant, si la longueur totale de l'adresse de messagerie et du nom d'affichage dépasse 255 caractères, le nom d'affichage doit être supprimé.
  
Les parties d'une adresse SMTP sont mappées aux propriétés MAPI de la manière suivante:
  
|**Composant d'adresse SMTP**|**Propriété MAPI**|
|:-----|:-----|
| _nom d'affichage_ de tous les destinataires  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _nom d'affichage_ du champ de  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _nom d'affichage_ du champ sender  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _adresse de messagerie_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implicite, Always "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
S'il n'existe pas de nom d'affichage pour une adresse sur le courrier entrant, l'adresse de messagerie complète doit être utilisée à la place. Le type d'adresse est toujours SMTP.
  
Les propriétés de destinataire sont extraites de la table de destinataires du message MAPI; les propriétés des expéditeurs sont extraites du message lui-même.
  

