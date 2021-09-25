---
title: Responsabilités d’attribution de noms de clients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: de707abc99393d40461e0f2be696040b570764d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584688"
---
# <a name="client-naming-responsibilities"></a>Responsabilités d’attribution de noms de clients

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients doivent respecter une convention d’attribution de noms pour leurs propriétés qui doivent être traduites par une passerelle. Toutes les propriétés à traduire doivent être créées en tant que propriétés nommées dans l’un des cinq jeux de propriétés désignés pour contenir les propriétés mappables :
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Les propriétés qui concernent le même utilisateur doivent avoir le même nom. Les passerelles s’appuient sur cette convention d’attribution de noms, qui leur permet de faire correspondre une adresse avec son type d’adresse correct. Pour l’analyse des adresses, le mappage entre l’adresse et le type d’adresse doit être précis.
  
Les propriétés nommées MAPI sont représentées par la structure de données **MAPINAMEID,** qui spécifie que le nom de la propriété peut être une chaîne Unicode ou un nombre entière 32 bits. Pour plus d’informations, [voir MAPINAMEID](mapinameid.md). Il est recommandé d’utiliser des noms d’ensembles pour les groupes d’adresses, car il s’agit d’un moyen simple de différencier les ensembles de propriétés mappables et peut facilement servir d’index à l’utilisateur. L’alternative à l’utilisation de nombres integers consiste à affecter une chaîne comme nom pour les cinq propriétés mappables d’un utilisateur. Si un seul utilisateur nécessite un mappage, l’affectation d’une chaîne est acceptable. Toutefois, lorsqu’il y a plusieurs utilisateurs, il est préférable d’utiliser l’attribution de noms de nombres multiples. Le nom, qu’il soit numérique ou chaîne, doit être stocké dans une propriété spécifique à une classe de message ou dans une propriété appartenant à un jeu de propriétés défini par l’application cliente. 
  
> [!NOTE]
> Évitez de traduire des noms de type integer en chaînes, telles que « route_recipient_1 » et « route_recipient_2 ». Cet effort est inutile. 
  
Pour illustrer le fonctionnement de cette convention d’attribution de noms, envisagez une application de routage qui envoie un message à chaque membre d’une équipe à quatre personnes. Lorsqu’un membre reçoit le message, il doit y répondre avant de pouvoir être envoyé avec les réponses compilées au membre suivant. Le message d’origine contient une liste de destinataires avec une entrée : le premier membre de l’équipe. Les propriétés de passerelle mappables des trois autres membres de l’équipe sont incorporées dans le message. Chaque membre possède cinq propriétés utilisateur principales résidant dans les jeux de propriétés de passerelle mappables, qui sont affectées à un numéro unique en tant que nom. 
  
Le tableau suivant illustre les paramètres de chaque ensemble de propriétés mappables de passerelle stockées pour les trois membres restants de l’équipe vers lesquels le message est acheminé lorsque le premier membre de l’équipe en a terminé.
  
|**Property Set**|**Second Team  <br/> Member**|**Troisième membre de  <br/> l’équipe**|**Quatrième membre de  <br/> l’équipe**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Adresse = 0  <br/> |Adresse = 1  <br/> |Adresse = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Type d’adresse = 0  <br/> |Type d’adresse = 1  <br/> |Type d’adresse = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nom complet = 0  <br/> |Nom complet = 1  <br/> |Nom complet = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Identificateur d’entrée = 0  <br/> |Identificateur d’entrée = 1  <br/> |Identificateur d’entrée = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Clé de recherche = 0  <br/> |Clé de recherche = 1  <br/> |Clé de recherche = 2  <br/> |
   
Les clients qui utilisent des clés de recherche mappables comme références à d’autres propriétés de message doivent reconnaître que les autres propriétés de message ne seront pas traduites, sauf si elles sont placées dans l’un de ces jeux de propriétés mappables. Lorsqu’un message avec des références non mappées à des clés de recherche mappées est envoyé à une destination dans un autre domaine de messagerie, les références ne sont pas valides. Pour que ces autres propriétés restent synchronisées avec les clés de recherche, vous pouvez leur attribuer des noms de chaînes dans le jeu de propriétés PS_ROUTING_SEARCH_KEY qui n’interfèrent pas avec les noms donnés aux propriétés mappables principales. Par exemple, supposons qu’un client doit transmettre une propriété qui contient la clé de recherche de la dernière personne dans une longue liste de routage. Le client peut créer une propriété nommée dans le jeu PS_ROUTING_SEARCH_KEY propriétés appelée « last_search_key ». Étant donné qu’elle est stockée dans un jeu de propriétés mappables, la propriété « last_search_key » est traduite avec le reste des propriétés mappables de passerelle.
  

