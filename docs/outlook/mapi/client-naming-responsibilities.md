---
title: Responsabilités du client d’attribution de noms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a97d108b2f36b40e5f8818ea81c138d7384ce9b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783049"
---
# <a name="client-naming-responsibilities"></a>Responsabilités du client d’attribution de noms

  
  
**S’applique à**: Outlook 
  
Les clients doivent respecter une convention d’affectation de noms pour leurs propriétés qui doivent être traduits par une passerelle. Toutes les propriétés à traduire doivent être créées en tant que propriétés nommées dans un des jeux de cinq propriété destinée à contenir les propriétés mappables :
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Recourir à des propriétés qui sont associées au même utilisateur doit être le même nom attribué. Passerelles reposent sur cette convention d’affectation de noms, qui leur permet de faire correspondre une adresse avec son type d’adresse approprié. Pour l’analyse de l’adresse, le mappage entre l’adresse et le type d’adresse doit être exactes.
  
MAPI nommée propriétés sont représentés par la structure de données **MAPINAMEID** , qui spécifie que le nom de la propriété peut être une chaîne Unicode ou un entier 32 bits. Pour plus d’informations, voir [MAPINAMEID](mapinameid.md). Entier naming est recommandé pour les groupes d’adresses car il s’agit d’une méthode simple pour différencier les jeux de propriétés mappables, il peut être facilement un index à l’utilisateur. L’alternative à l’utilisation des entiers consiste à attribuer une chaîne en tant que le nom de toutes les cinq propriétés mappables d’un utilisateur. Si un utilisateur requiert un mappage, attribution d’une chaîne est acceptable. Toutefois, lorsqu’il existe plusieurs utilisateurs, il est préférable d’utiliser des noms entier. Le nom, qu’il s’agisse de chiffres ou chaîne, doit être stocké dans une propriété de spécifiques à la classe de message ou dans une propriété appartenant à un jeu de propriétés qui est défini par l’application cliente. 
  
> [!NOTE]
> Éviter la traduction des noms entier à des chaînes, telles que « route_recipient_1 » et « route_recipient_2 ». Cette tâche n’est pas nécessaire. 
  
Pour illustrer le fonctionne de cette convention d’affectation de noms, envisagez d’une application de routage qui envoie un message à chaque membre d’une équipe de quatre personnes. Lorsqu’un membre reçoit le message, qu’il doit y répondre avant de pouvoir envoyer ainsi que les réponses compilées vers le membre suivant. Le message d’origine contient une liste de destinataires avec une seule entrée : le premier membre de l’équipe. Incorporé dans le message sont les propriétés de passerelle-mappables pour les trois autres membres d’équipe. Chaque membre a cinq propriétés de l’utilisateur principal qui résident dans les jeux de propriétés de passerelle-mappables, qui sont affectés à un numéro unique en tant que nom. 
  
Le tableau suivant illustre les paramètres pour chaque jeu de propriétés de passerelle-mappables stockées pour les trois restant de membres de l’équipe à qui le message est routé lorsque le premier membre de l’équipe est terminé avec lui.
  
|**Ensemble de propriétés**|**Deuxième équipe <br/> membre**|**Troisième d’équipe <br/> membre**|**Quatrième de l’équipe <br/> membre**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Adresse = 0  <br/> |Adresse = 1  <br/> |Adresse = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Type d’adresse = 0  <br/> |Type d’adresse = 1  <br/> |Type d’adresse = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nom complet = 0  <br/> |Nom complet = 1  <br/> |Nom complet = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Identificateur d’entrée = 0  <br/> |Identificateur d’entrée = 1  <br/> |Identificateur d’entrée = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Clé de recherche = 0  <br/> |Clé de recherche = 1  <br/> |Clé de recherche = 2  <br/> |
   
Les clients qui utilisent des clés de recherche mappables en tant que références à d’autres propriétés de message doivent reconnaître que les autres propriétés de message ne seront pas traduites, sauf si elles sont placées dans une de ces jeux de propriétés mappables. Lorsqu’un message avec des références non mappés aux clés de recherche mappé est envoyé vers une destination dans un autre domaine de messagerie, les références sont incorrectes. Pour activer les autres propriétés sont synchronisés avec les clés de recherche, vous pouvez les assigner des noms de chaîne dans le jeu de propriétés PS_ROUTING_SEARCH_KEY qui n’interfèrent pas portant le nom donné à n’importe quelle mappables principaux. Par exemple, supposons qu’un client doit transmettre une propriété qui contient la clé de recherche pour la dernière personne dans une liste de routage long. Le client peut créer une propriété nommée dans le jeu de propriétés PS_ROUTING_SEARCH_KEY appelé « last_search_key ». Parce qu’il est stocké dans un jeu de propriétés mappables, est traduite par la propriété « last_search_key » avec le reste des propriétés mappables-passerelle.
  

