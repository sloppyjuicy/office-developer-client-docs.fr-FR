---
title: Propriétés de passerelle mappables
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b637f4921165d70ddeda914b4299c35aabe8218f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783390"
---
# <a name="gateway-mappable-properties"></a>Propriétés de passerelle mappables

**S’applique à**: Outlook 
  
Passerelle-mappables les propriétés qui peuvent nécessiter traduction lorsque envoyés à partir d’un domaine de messagerie à l’autre. Propriétés de passerelle-mappables de MAPI autoriser les messages inclure des informations qui requiert une passerelle pour garantir la destination de système de messagerie utilise correctement. Bien que les développeurs de passerelle ne sont pas tenus de fournir cette fonctionnalité de traduction, ils doivent envisager passerelle-mappables propriétés comme une opportunité pour améliorer la gestion du contenu du message.
  
MAPI spécifie cinq types de propriétés de passerelle-mappables :
  
- Nom d’affichage
    
- Adresse de messagerie
    
- Type de messagerie
    
- Identificateur d’entrée
    
- Clé de recherche
    
Il s’agit de l’ensemble des propriétés qui sont associées à des destinataires, les expéditeurs, destinataires des rapports et déléguées expéditeurs et destinataires d’adressage. Pour vous aider à votre client de définir ces propriétés afin qu’une passerelle gère les spécialement, MAPI spécifie une convention d’affectation de noms à l’aide des propriétés nommées et les jeux de propriétés. Il existe cinq jeux de propriétés pour contenir des propriétés nommées, les propriétés d’adressage qui nécessitent un mappage. Il existe une propriété définie pour chaque type de propriété mappable. Les jeux de propriétés qui contiendront ces propriétés adressage sont les suivants :
  
|**Jeu de propriétés**|**Description**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Contient les propriétés de chaîne utilisées comme noms complets.  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Contient les propriétés de chaîne utilisées comme adresses de messagerie.  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Contient les propriétés de chaîne utilisées en tant que types d’adresse de messagerie.  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Contient des propriétés binaires utilisées comme les identificateurs d’entrée à long terme.  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Contient des propriétés binaires utilisées en tant que clés de recherche.  <br/> |
   

