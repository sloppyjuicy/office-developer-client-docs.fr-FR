---
title: Adresses SMTP
description: Décrit une forme particulière d’adresse RFC 822 qui encode le mieux les adresses MAPI dans Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
ms.openlocfilehash: 3fed50498779bd81e852e2a5b423b7f609ccae45
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894353"
---
# <a name="smtp-addresses"></a>Adresses SMTP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le format des adresses e-mail SMTP est défini dans RFC 822. Les composants MAPI doivent gérer n’importe quelle adresse conforme à cette norme. Toutefois, il existe une forme particulière d’adresse RFC 822 qui encode le mieux les adresses MAPI :
  
 _display-name_ **\<** _email-address_ **\>**
  
Les crochets d’angle sont inclus en tant que littéraux. Les espaces vides sont courants dans les noms d’affichage ; ils n’ont pas besoin d’être cités. Une adresse standard peut ressembler à celle-ci, qui appartient à l’un des coauteurs de RFC 1521 :
  
Nathaniel Borenstein \<nsb@bellcore.com\>
  
Si le nom d’affichage contient des caractères qui ont une signification spéciale dans les adresses SMTP, par \< exemple ou @, le nom complet de l’affichage doit être placé entre guillemets doubles. Dans le courrier sortant, si la longueur totale de l’adresse e-mail et du nom d’affichage dépasse 255 caractères, le nom d’affichage doit être supprimé.
  
Les parties d’un mappage d’adresses SMTP dans les propriétés MAPI sont les suivantes :
  
|**Composant d’adresse SMTP**|**MapI, propriété**|
|:-----|:-----|
| _display-name_ pour tous les destinataires  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _display-name_ for From field  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _display-name_ pour le champ Expéditeur  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _adresse e-mail_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implicite, toujours « SMTP »  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
S’il n’existe aucun nom d’affichage pour une adresse sur le courrier entrant, l’adresse e-mail entière doit être utilisée à la place. Le type d’adresse est toujours SMTP.
  
Les propriétés du destinataire sont extraites de la table des destinataires du message MAPI ; les propriétés de l’expéditeur sont extraites du message lui-même.
  

