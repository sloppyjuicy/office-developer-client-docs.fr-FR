---
title: Propriétés mappables de la passerelle
description: Cet article fournit une vue d’ensemble des propriétés mappables de passerelle.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
ms.openlocfilehash: e4056dec7c03af132b0ea41a3f77813dcf606f93
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812459"
---
# <a name="gateway-mappable-properties"></a>Propriétés mappables de la passerelle

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les propriétés mappables par passerelle sont des propriétés qui peuvent nécessiter une traduction lorsqu’elles sont envoyées d’un domaine de messagerie à un autre. Les propriétés mappables de la passerelle MAPI permettent aux messages d’inclure des informations qui nécessitent une passerelle pour garantir que le système de messagerie de destination l’utilise correctement. Bien que les développeurs de passerelles ne soient pas tenus de fournir cette fonctionnalité de traduction, ils doivent considérer les propriétés mappables par passerelle comme une occasion d’améliorer la gestion du contenu des messages.
  
MAPI spécifie cinq types de propriétés mappables par passerelle :
  
- Nom unique (DN)
    
- Nom complet
    
- Type d’e-mail
    
- Identificateur d’entrée
    
- Clé de recherche
    
Il s’agit de l’ensemble des propriétés d’adressage associées aux destinataires, expéditeurs, destinataires de rapports et expéditeurs délégués et destinataires. Pour aider votre client à définir ces propriétés afin qu’une passerelle les gère spécialement, MAPI spécifie une convention d’affectation de noms à l’aide de propriétés nommées et de jeux de propriétés. Cinq ensembles de propriétés contiennent des propriétés nommées, les propriétés d’adressage qui nécessitent un mappage. Il existe une propriété définie pour chaque type de propriété mappable. Les ensembles de propriétés qui contiendront ces propriétés d’adressage nommées sont les suivants.
  
|**Jeu de propriétés**|**Description**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |Contient les propriétés de chaîne utilisées comme noms d’affichage. |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Contient les propriétés de chaîne utilisées comme adresses e-mail. |
|PS_ROUTING_ADDRTYPE  <br/> |Contient les propriétés de chaîne utilisées comme types d’adresse e-mail. |
|PS_ROUTING_ENTRYID  <br/> |Contient des propriétés binaires utilisées comme identificateurs d’entrée à long terme. |
|PS_ROUTING_SEARCH_KEY  <br/> |Contient les propriétés binaires utilisées comme clés de recherche. |
   

