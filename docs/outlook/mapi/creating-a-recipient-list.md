---
title: Création d'une liste de destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428213"
---
# <a name="creating-a-recipient-list"></a>Création d'une liste de destinataires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une liste de destinataires est une structure [ADRLIST](adrlist.md) qui contient un tableau de structures de valeurs de propriétés pour chaque destinataire de message: destination du message. Un destinataire peut représenter un utilisateur humain, un ordinateur ou un dossier. Tous les messages à envoyer nécessitent au moins un destinataire qui a été redirigé par le processus de résolution de noms, ce qui permet de s'assurer que la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est incluse dans le tableau de valeurs de la propriété du destinataire. 
  
Les propriétés d'un destinataire sont une combinaison de propriétés de carnet d'adresses et de propriétés de message. Les propriétés du destinataire peuvent s'appliquer soit à tous les messages pour un destinataire particulier, soit uniquement au message actif. Les fournisseurs de banque de messages et de transport peuvent définir les propriétés des destinataires. 
  
Chaque destinataire doit disposer d'un ensemble principal de propriétés dans son tableau de valeurs de propriétés, au moment où le message est prêt à être envoyé. Les propriétés de destinataire requises sont les suivantes:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Ces propriétés sont utilisées pour accéder au destinataire, lui envoyer des messages et pour le comparer à d'autres. Toutes ces propriétés ne doivent pas être disponibles immédiatement. Vous pouvez ajouter un destinataire initialement sans connaître son identificateur d'entrée, en utilisant le processus de résolution de noms pour affecter cette propriété. À un moment donné, avant d'envoyer un message, appelez [IAddrBook:: ResolveName](iaddrbook-resolvename.md) pour vous assurer que tous les destinataires de votre liste de destinataires sont résolus. Pour plus d'informations, consultez la rubrique relative à [la résolution d'un nom de destinataire](resolving-a-recipient-name.md).
  
Les listes de destinataires peuvent être créées à partir d'utilisateurs de messagerie ou d'entrées de liste de distribution dans un conteneur de carnet d'adresses ou à partir de plusieurs points. Les destinataires uniques sont créés en tant qu'entrées temporaires pour être utilisés uniquement pour l'adressage d'un seul message ou comme entrées à ajouter à un carnet d'adresses personnel. Le format d'un identificateur d'entrée unique et d'une adresse est défini par MAPI. Pour plus d'informations sur ces formats, consultez les [adresses ponctuelles](one-off-addresses.md) et les identificateurs d' [entrée ponctuelle](one-off-entry-identifiers.md).
  
Vous pouvez permettre aux utilisateurs de créer leurs listes de destinataires:
  
- Uniquement avec les entrées du carnet d'adresses.
    
- Uniquement avec les entrées uniques.
    
- Avec une combinaison de destinataires de carnet d'adresses et de personnes à un.
    
 **Pour créer une liste de destinataires à l'aide de la boîte de dialogue adresse commune**
  
1. AlLouez une structure [ADRPARM](adrparm.md) et un pointeur vers une structure [ADRLIST](adrlist.md) . 
    
2. Zéro de la mémoire dans la structure **ADRPARM** et définissez le pointeur **ADRLIST** sur null. 
    
3. Appelez [IAddrBook:: Address](iaddrbook-address.md) pour afficher la boîte de dialogue d'adresses et remplir la structure **ADRPARM** . 
    
4. Appelez [IMessage:: ModifyRecipients](imessage-modifyrecipients.md), en passant le pointeur **ADRLIST** . Cette structure contient les propriétés de chacun des destinataires sélectionnés par l'utilisateur. 
    
 **Pour créer une liste de destinataires par programme**
  
1. AlLouez une structure **ADRLIST** qui contient une structure [ADRENTRY](adrentry.md) pour chacun des destinataires à inclure dans la liste. Rendez chaque structure **ADRENTRY** suffisamment importante pour contenir chacune des propriétés requises et **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).
    
2. Pour chaque destinataire, définissez le tableau de valeurs de propriété pour son membre **aEntries** dans la structure **ADRLIST** . 
    
3. Appelez [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) avec l'indicateur MODRECIP_ADD défini. 
    

