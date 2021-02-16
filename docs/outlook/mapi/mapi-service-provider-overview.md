---
title: Vue d’ensemble du fournisseur de services MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: bc25158daa9579b5cd6cebe1eee878bf087762a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431427"
---
# <a name="mapi-service-provider-overview"></a>Vue d’ensemble du fournisseur de services MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les différents fournisseurs de services sont entre le sous-système MAPI et les systèmes de messagerie. Les fournisseurs de services sont comme des pilotes qui connectent des applications clientes MAPI à un système de messagerie sous-jacent. Il existe trois types de fournisseurs : fournisseurs de magasins de messages, fournisseurs de carnet d’adresses ou d’annuaire, et fournisseurs de transport de messages. MAPI prend en charge chaque type de service indépendamment, ce qui permet à un fournisseur de proposer un ou plusieurs fournisseurs de services personnalisés. Par exemple, un fournisseur peut créer un fournisseur de carnet d’adresses qui utilise un annuaire téléphonique d’entreprise des employés ou créer un fournisseur de banque de messages qui utilise une base de données existante.
  
Les fournisseurs de services sont généralement écrits pour des systèmes de messagerie spécifiques par des développeurs de logiciels qui ont des connaissances ou une expérience spécialisées avec un système particulier. Par exemple, Microsoft Outlook 2013 et Microsoft Outlook 2010 Mobile Services utilisent un fournisseur de carnet d’adresses pour exposer un carnet d’adresses mobile dans Outlook. 
  
MAPI présente aux applications clientes un affichage unifié des informations du carnet d’adresses et du fournisseur de transport. Cette approche intégrée empêche l’application cliente d’avoir à ma router les données vers le fournisseur approprié. Cela empêche également l’utilisateur d’avoir à négocier entre plusieurs schémas d’adressan de carnet d’adresses et de fournisseur de transport. Toutefois, les informations sur les fournisseurs de magasins de messages ne sont pas unifiées et les clients qui utilisent plusieurs fournisseurs de magasins de messages sont chargés de les gérer individuellement.
  
Les fournisseurs de services fonctionnent avec MAPI pour créer et envoyer des messages de la manière suivante : les messages sont créés à l’aide d’un formulaire approprié pour le type ou la classe spécifique du message. De nombreux messages sont effectués avec le formulaire de note standard qui est livré avec le sous-système MAPI, soit par l’utilisateur d’une application cliente, soit par programme sans interaction de l’utilisateur. Le message terminé est adressé à un ou plusieurs destinataires : un utilisateur ou un groupe d’utilisateurs désignés pour recevoir le message. Un destinataire peut ou non avoir une entrée dans un répertoire qui appartient à l’un des fournisseurs de carnets d’adresses installés. Les destinataires qui ne sont pas associés à un fournisseur de carnet d’adresses installé sont appelés destinataires personnalisés ou adresses personnalisées. Une adresse unique peut être temporaire et ne durer que jusqu’à l’envoi du message. 
  
Lorsque l’application cliente envoie le message, le fournisseur de magasins de messages vérifie que chaque destinataire possède une adresse unique et valide et que le message dispose de toutes les informations nécessaires à la transmission. S’il existe une question sur un destinataire (par exemple, lorsqu’il existe plusieurs destinataires du même nom), un fournisseur de carnet d’adresses s’occupe de résoudre l’ambiguïté. Le message est ensuite placé dans la file d’attente sortante. 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalités et architecture MAPI](mapi-features-and-architecture.md)

