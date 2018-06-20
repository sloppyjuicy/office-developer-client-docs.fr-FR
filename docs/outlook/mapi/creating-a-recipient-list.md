---
title: Création d’une liste de destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fa23377a8b080ae9dac3e31dfa137ca03a242c74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783124"
---
# <a name="creating-a-recipient-list"></a>Création d’une liste de destinataires

  
  
**S’applique à**: Outlook 
  
Une liste de destinataires est une structure [ADRLIST](adrlist.md) qui contient un tableau de structures de valeur de propriété pour chaque destinataire du message — destination pour le message. Un destinataire peut représenter un utilisateur, un ordinateur ou un dossier. Tous les messages soient envoyées nécessitent au moins un destinataire qui a été par le biais du processus de résolution de nom, un processus pour s’assurer que la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est incluse dans le tableau de valeurs de propriété du destinataire. 
  
Les propriétés d’un destinataire sont une combinaison de propriétés de carnet d’adresses et les propriétés de message. Propriétés de destinataire peuvent s’appliquent à tous les messages pour un destinataire particulier ou uniquement pour le message en cours. Les deux messages magasin et fournisseurs de transport peuvent définir des propriétés de destinataire. 
  
Chaque destinataire doit avoir un ensemble de propriétés dans le tableau de valeurs de propriété au moment où que le message est prêt à être envoyé. Le jeu de propriétés de destinataire requis sont les suivants :
  
- **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Ces propriétés sont utilisées pour accéder au destinataire, lui envoyer des messages et comparer à d’autres personnes. Toutes ces propriétés doivent être immédiatement disponibles. Vous pouvez ajouter un destinataire à l’origine sans connaître son identificateur d’entrée, compter sur le processus de résolution de noms à assigner à cette propriété. À un moment donné avant d’envoyer un message, appelez [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour vous assurer que tous les destinataires dans votre liste des destinataires sont résolus. Pour plus d’informations, voir [résolution de nom d’un destinataire](resolving-a-recipient-name.md).
  
Listes de destinataires peuvent être créés à partir d’utilisateurs ou des entrées de liste de distribution dans un conteneur de carnet d’adresses de messagerie ou uniques. Uniques sont des destinataires qui sont créés comme des entrées temporaires à utiliser uniquement pour adresser un message unique ou comme des entrées à ajouter à un carnet d’adresses personnel. Le format d’un identificateur d’entrée unique et une adresse est défini par MAPI. Pour plus d’informations sur ces formats, voir [Adresses uniques](one-off-addresses.md) et des [Identificateurs uniques d’entrée](one-off-entry-identifiers.md).
  
Vous pouvez permettre aux utilisateurs créer leurs listes de destinataires :
  
- Uniquement avec les entrées du carnet d’adresses.
    
- Uniquement avec les entrées uniques.
    
- Avec une combinaison de destinataires de carnet d’adresses et uniques.
    
 **Pour créer une liste de destinataires à l’aide de la boîte de dialogue adresse**
  
1. Allouez une structure [ADRPARM](adrparm.md) et un pointeur vers une structure [ADRLIST](adrlist.md) . 
    
2. Zéro de la mémoire dans la structure **ADRPARM** et définir le pointeur **ADRLIST** NULL. 
    
3. Appelez [IAddrBook::Address](iaddrbook-address.md) pour afficher la boîte de dialogue adresse et remplir la structure **ADRPARM** . 
    
4. Appelez [IMessage::ModifyRecipients](imessage-modifyrecipients.md), en passant le pointeur **ADRLIST** . Cette structure contient les propriétés de chacun des destinataires sélectionnés par l’utilisateur. 
    
 **Pour créer une liste de destinataires par programme**
  
1. Allouez une structure **ADRLIST** qui contient une structure [ADRENTRY](adrentry.md) pour chacun des destinataires à inclure dans la liste. Vérifiez chaque structure **ADRENTRY** suffisante pour contenir chacune des propriétés requises et **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).
    
2. Pour chaque destinataire, définissez le tableau de valeurs de propriété pour ses membres **aEntries** dans la structure **ADRLIST** . 
    
3. Appelez [IMessage::ModifyRecipients](imessage-modifyrecipients.md) avec l’indicateur MODRECIP_ADD. 
    

