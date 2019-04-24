---
title: Responsabilités de dénomination des clients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 808c7abf3d29872a8c5095fdc6dc39b2107a8993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335139"
---
# <a name="client-naming-responsibilities"></a>Responsabilités de dénomination des clients

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients doivent respecter une convention d'affectation de noms pour leurs propriétés qui doivent être traduites par une passerelle. Toutes les propriétés à traduire doivent être créées en tant que propriétés nommées dans l'un des cinq jeux de propriétés désignés pour contenir les propriétés mappées:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Les propriétés d'adressage qui concernent le même utilisateur doivent avoir le même nom. Les passerelles s'appuient sur cette Convention d'affectation de noms, qui leur permet de correspondre à une adresse dont le type d'adresse est correct. Pour l'analyse syntaxique des adresses, le mappage entre l'adresse et le type d'adresse doit être exact.
  
Les propriétés nommées MAPI sont représentées par la structure de données **MAPINAMEID** , qui spécifie que le nom de la propriété peut être une chaîne Unicode ou un nombre entier de 32 bits. Pour plus d'informations, consultez la rubrique [MAPINAMEID](mapinameid.md). La dénomination des nombres enTiers est recommandée pour les groupes d'adresses, car il s'agit d'un moyen simple de différencier les ensembles de propriétés pouvant être mappés et peut facilement servir d'index à l'utilisateur. L'alternative à l'utilisation d'entiers est d'assigner une chaîne comme nom pour les cinq propriétés mappable d'un utilisateur. Si un seul utilisateur doit être mappé, l'affectation d'une chaîne est acceptable. Toutefois, lorsqu'il y a plusieurs utilisateurs, il est préférable d'utiliser des noms d'entiers. Le nom, qu'il soit numérique ou basé sur une chaîne, doit être stocké dans une propriété spécifique à la classe de message ou dans une propriété appartenant à un jeu de propriétés défini par l'application cliente. 
  
> [!NOTE]
> Évitez de traduire des noms d'entiers en chaînes, par exemple «route_recipient_1» et «route_recipient_2». Cet effort n'est pas nécessaire. 
  
Pour illustrer le fonctionnement de cette Convention d'affectation de noms, considérez une application de routage qui envoie un message à chaque membre d'une équipe de quatre personnes. Lorsqu'un membre reçoit le message, il doit y répondre avant de pouvoir l'envoyer avec les réponses compilées au membre suivant. Le message d'origine contient une liste de destinataires avec une entrée: le premier membre de l'équipe. Les propriétés intégrées à la passerelle pour les trois autres membres de l'équipe sont incorporées dans le message. Chaque membre dispose de cinq propriétés utilisateur de base résidant dans les ensembles de propriétés mappés avec la passerelle, qui sont affectées d'un numéro unique en tant que nom. 
  
Le tableau suivant illustre les paramètres de chaque jeu de propriétés mappées à la passerelle stockées pour les trois autres membres de l'équipe auxquels le message est acheminé lorsque le premier membre de l'équipe a fini de l'utiliser.
  
|**Property Set**|**Deuxième membre <br/> de l'équipe**|**Troisième membre <br/> de l'équipe**|**Quatrième membre <br/> d'équipe**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Adresse = 0  <br/> |Adresse = 1  <br/> |Adresse = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Type d'adresse = 0  <br/> |Type d'adresse = 1  <br/> |Type d'adresse = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nom complet = 0  <br/> |Nom complet = 1  <br/> |Nom complet = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Identificateur d'entrée = 0  <br/> |Identificateur d'entrée = 1  <br/> |Identificateur d'entrée = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Clé de recherche = 0  <br/> |Clé de recherche = 1  <br/> |Clé de recherche = 2  <br/> |
   
Les clients qui utilisent des clés de recherche mappées comme références à d'autres propriétés de message doivent reconnaître que les autres propriétés de message ne seront pas traduites, sauf si elles sont placées dans l'un de ces jeux de propriétés mappés. Lorsqu'un message avec des références non mappées vers des clés de recherche mappées est envoyé à une destination dans un autre domaine de messagerie, les références ne sont pas valides. Pour permettre à ces autres propriétés de rester synchronisées avec les clés de recherche, vous pouvez leur attribuer des noms de chaîne dans le jeu de propriétés PS_ROUTING_SEARCH_KEY qui n'interfèrent pas avec les noms attribués aux propriétés mappables principales. Par exemple, supposons qu'un client a besoin de transmettre une propriété qui contient la clé de recherche pour la dernière personne dans une longue liste de routage. Le client peut créer une propriété nommée dans le jeu de propriétés PS_ROUTING_SEARCH_KEY appelé «last_search_key». Étant donné qu'elle est stockée dans un jeu de propriétés mappé, la propriété «last_search_key» est traduite en même temps que les autres propriétés mappées sur la passerelle.
  

