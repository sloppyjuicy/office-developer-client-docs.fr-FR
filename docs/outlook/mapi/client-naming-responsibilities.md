---
title: Responsabilités de nommage du client
description: Toutes les propriétés à traduire doivent être créées en tant que propriétés nommées dans l’un des cinq ensembles désignés pour contenir des propriétés mappables.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
ms.openlocfilehash: 9e2404f306ab25d95554230f3cc5f94f7f58db27
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817563"
---
# <a name="client-naming-responsibilities"></a>Responsabilités de nommage du client

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients doivent suivre une convention d’affectation de noms pour leurs propriétés qui doivent être traduites par une passerelle. Toutes les propriétés à traduire doivent être créées en tant que propriétés nommées dans l’un des cinq jeux de propriétés désignés pour contenir des propriétés mappables :
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Les propriétés d’adressage qui se rapportent au même utilisateur doivent avoir le même nom. Les passerelles s’appuient sur cette convention d’affectation de noms, qui leur permet de faire correspondre une adresse à son type d’adresse correct. Pour l’analyse des adresses, le mappage entre l’adresse et le type d’adresse doit être précis.
  
Les propriétés nommées MAPI sont représentées par la structure de données **MAPINAMEID** , qui spécifie que le nom de la propriété peut être une chaîne Unicode ou un entier 32 bits. Pour plus d’informations, consultez [MAPINAMEID](mapinameid.md). Le nommage d’entier est recommandé pour les groupes d’adresses, car il s’agit d’un moyen simple de faire la distinction entre les ensembles de propriétés mappables, et il peut facilement servir d’index à l’utilisateur. L’alternative à l’utilisation d’entiers consiste à attribuer une chaîne comme nom pour les cinq propriétés mappables d’un utilisateur. Si un seul utilisateur nécessite un mappage, l’affectation d’une chaîne est acceptable. Toutefois, lorsqu’il y a plusieurs utilisateurs, il est préférable d’utiliser le nommage entier. Le nom, qu’il soit numérique ou basé sur une chaîne, doit être stocké dans une propriété spécifique à la classe de message ou dans une propriété appartenant à un jeu de propriétés défini par l’application cliente. 
  
> [!NOTE]
> Évitez de traduire des noms entiers en chaînes, telles que « route_recipient_1 » et « route_recipient_2 ». Cet effort n’est pas nécessaire. 
  
Pour illustrer le fonctionnement de cette convention d’affectation de noms, envisagez une application de routage qui envoie un message à chaque membre d’une équipe de quatre personnes. Lorsqu’un membre reçoit le message, il doit y répondre avant de pouvoir l’envoyer avec les réponses compilées au membre suivant. Le message d’origine contient une liste de destinataires avec une entrée : le premier membre de l’équipe. Les propriétés mappables de passerelle pour les trois autres membres de l’équipe sont incorporées dans le message. Chaque membre a cinq propriétés utilisateur principales résidant dans les ensembles de propriétés mappables de passerelle, qui se voient attribuer un nombre unique en tant que nom. 
  
Le tableau suivant illustre les paramètres de chaque ensemble de propriétés mappables par passerelle stockées pour les trois membres restants de l’équipe vers lesquels le message est acheminé lorsque le premier membre de l’équipe en a terminé avec celui-ci.
  
|**Property Set**|**Second Team  <br/> Member**|**Troisième membre de l’équipe <br/>**|**Quatrième membre de l’équipe <br/>**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Adresse = 0  <br/> |Adresse = 1  <br/> |Adresse = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Type d’adresse = 0  <br/> |Type d’adresse = 1  <br/> |Type d’adresse = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nom d’affichage = 0  <br/> |Nom d’affichage = 1  <br/> |Nom d’affichage = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Identificateur d’entrée = 0  <br/> |Identificateur d’entrée = 1  <br/> |Identificateur d’entrée = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Clé de recherche = 0  <br/> |Clé de recherche = 1  <br/> |Clé de recherche = 2  <br/> |
   
Les clients qui utilisent des clés de recherche mappables comme références à d’autres propriétés de message doivent reconnaître que les autres propriétés de message ne seront pas traduites, sauf si elles sont placées dans l’un de ces ensembles de propriétés mappables. Lorsqu’un message avec des références non mappées à des clés de recherche mappées est envoyé à une destination dans un autre domaine de messagerie, les références ne sont pas valides. Pour permettre à ces autres propriétés de rester synchronisées avec les clés de recherche, vous pouvez leur attribuer des noms de chaîne dans le jeu de propriétés PS_ROUTING_SEARCH_KEY qui n’interfère pas avec les noms donnés à l’une des propriétés mappables principales. Par exemple, supposons qu’un client doit transmettre une propriété qui contient la clé de recherche de la dernière personne d’une longue liste de routage. Le client peut créer une propriété nommée dans le jeu de propriétés PS_ROUTING_SEARCH_KEY appelé « last_search_key ». Étant donné qu’elle est stockée dans un jeu de propriétés mappable, la propriété « last_search_key » est traduite avec le reste des propriétés mappables de passerelle.
  

