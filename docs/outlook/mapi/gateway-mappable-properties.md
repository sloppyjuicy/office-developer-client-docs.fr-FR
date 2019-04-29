---
title: Propriétés mappables de la passerelle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430475"
---
# <a name="gateway-mappable-properties"></a>Propriétés mappables de la passerelle

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les propriétés pouvant être mappées par une passerelle sont des propriétés qui peuvent nécessiter une traduction lorsqu'elles sont envoyées d'un domaine de messagerie à un autre. Les propriétés pouvant être mappées par la passerelle MAPI permettent aux messages d'inclure des informations qui nécessitent une passerelle pour s'assurer que le système de messagerie de destination l'utilise correctement. Bien que les développeurs de passerelles ne soient pas tenus de fournir cette fonctionnalité de traduction, ils doivent envisager des propriétés mappées sur les passerelles pour améliorer la gestion du contenu des messages.
  
MAPI spécifie cinq types de propriétés mappées sur la passerelle:
  
- Nom unique (DN)
    
- Nom complet
    
- Type de courrier électronique
    
- Identificateur d'entrée
    
- Clé de recherche
    
Il s'agit de l'ensemble des propriétés d'adressage associées aux destinataires, aux expéditeurs, aux destinataires des rapports, ainsi qu'aux expéditeurs et destinataires délégués. Pour aider votre client à définir ces propriétés de sorte qu'une passerelle les gère spécialement, MAPI spécifie une convention d'affectation de noms à l'aide de propriétés nommées et de jeux de propriétés. Cinq jeux de propriétés existent pour contenir les propriétés nommées, les propriétés d'adressage qui nécessitent un mappage. Il existe un jeu de propriétés pour chaque type de propriété mappable. Les jeux de propriétés qui contiendront ces propriétés d'adressage nommées sont les suivants.
  
|**Jeu de propriétés**|**Description**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Contient les propriétés de chaîne utilisées en tant que noms complets.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Contient les propriétés de chaîne utilisées en tant qu'adresses de messagerie.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Contient les propriétés de chaîne utilisées comme types d'adresses de messagerie.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Contient les propriétés binaires utilisées en tant qu'identificateurs d'entrée à long terme.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Contient les propriétés binaires utilisées en tant que clés de recherche.  <br/> |
   

