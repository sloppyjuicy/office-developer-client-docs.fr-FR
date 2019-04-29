---
title: Vue d'ensemble du fournisseur de services MAPI
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
# <a name="mapi-service-provider-overview"></a>Vue d'ensemble du fournisseur de services MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Entre le sous-système MAPI et les systèmes de messagerie sont les différents fournisseurs de services. Les fournisseurs de services sont similaires aux pilotes qui connectent les applications clientes MAPI à un système de messagerie sous-jacent. Il existe trois types de fournisseurs: les fournisseurs de banque de messages, le carnet d'adresses ou les fournisseurs d'annuaire et les fournisseurs de transport de messages. MAPI prend en charge chaque type de service indépendamment, ce qui permet à un fournisseur de proposer un ou plusieurs fournisseurs de services personnalisés. Par exemple, un fournisseur peut souhaiter créer un fournisseur de carnets d'adresses qui utilise un annuaire d'entreprise de répertoire téléphonique d'employés ou créer un fournisseur de banque de messages qui utilise une base de données existante.
  
Les fournisseurs de services sont généralement écrits pour des systèmes de messagerie spécifiques par des développeurs de logiciels qui ont des connaissances ou une expérience spécialisées avec un système particulier. Par exemple, les services mobiles Microsoft Outlook 2013 et Microsoft Outlook 2010 utilisent un fournisseur de carnet d'adresses pour exposer un carnet d'adresses mobile dans Outlook. 
  
MAPI présente les applications clientes avec une vue unifiée des informations du carnet d'adresses et du fournisseur de transport. Cette approche intégrée empêche l'application cliente de mapper les données au fournisseur approprié. Elle empêche également l'utilisateur d'avoir à négocier plusieurs modèles d'adressage de carnet d'adresses et de fournisseur de transport. Toutefois, les informations du fournisseur de banque de messages ne sont pas unifiées, et les clients qui utilisent plusieurs fournisseurs de banques de messages sont responsables de leur gestion individuelle.
  
Les fournisseurs de services fonctionnent avec MAPI pour créer et envoyer des messages de la manière suivante: les messages sont créés à l'aide d'un formulaire approprié pour le type spécifique ou la classe de message. De nombreux messages sont créés avec le formulaire de note standard qui est fourni avec le sous-système MAPI, soit par l'utilisateur d'une application client, soit par programme sans intervention de l'utilisateur. Le message terminé est adressé à un ou plusieurs destinataires (un utilisateur ou un groupe d'utilisateurs désigné pour recevoir le message). Un destinataire peut avoir ou non une entrée dans un répertoire auquel l'un des fournisseurs de carnet d'adresses installé est propriétaire. Les destinataires qui ne sont pas associés à un fournisseur de carnet d'adresses installé sont appelés destinataires personnalisés ou adresses ponctuelles. Une adresse ponctuelle peut être temporaire, ne durer que jusqu'à ce que le message soit envoyé. 
  
Lorsque l'application cliente envoie le message, le fournisseur de banque de messages vérifie que chaque destinataire possède une adresse unique et valide et que le message contient toutes les informations nécessaires à la transmission. S'il y a une question à propos d'un destinataire (par exemple, lorsqu'il y a plusieurs destinataires ayant le même nom), un fournisseur de carnets d'adresses prend en charge la résolution de l'ambiguïté. Le message est ensuite placé dans la file d'attente sortante. 
  
## <a name="see-also"></a>Voir aussi



[Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)

