---
title: Vue d’ensemble du fournisseur de services MAPI
description: Donne une vue d’ensemble des fournisseurs de services MAPI, qui sont comme des pilotes qui connectent des applications clientes MAPI à un système de messagerie sous-jacent.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
ms.openlocfilehash: 62c4be98fa8338a29d2b1cf3e94465938200c337
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828331"
---
# <a name="mapi-service-provider-overview"></a>Vue d’ensemble du fournisseur de services MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Entre le sous-système MAPI et les systèmes de messagerie se trouvent les différents fournisseurs de services. Les fournisseurs de services sont comme des pilotes qui connectent des applications clientes MAPI à un système de messagerie sous-jacent. Il existe trois types de fournisseurs : les fournisseurs de magasins de messages, les fournisseurs de carnet d’adresses ou d’annuaires et les fournisseurs de transport de messages. MAPI prend en charge chaque type de service indépendamment, ce qui permet à un fournisseur d’offrir un ou plusieurs fournisseurs de services personnalisés. Par exemple, un fournisseur peut vouloir créer un fournisseur de carnets d’adresses qui utilise un annuaire de carnets téléphoniques d’entreprise d’employés ou créer un fournisseur de magasin de messages qui utilise une base de données existante.
  
Les fournisseurs de services sont généralement écrits pour des systèmes de messagerie spécifiques par des développeurs de logiciels qui ont des connaissances ou une expérience spécialisées avec un système particulier. Par exemple, les Microsoft Outlook 2013 et les Microsoft Outlook 2010 Mobile Services utilisent un fournisseur de carnets d’adresses pour exposer un carnet d’adresses mobiles dans Outlook. 
  
MAPI présente aux applications clientes une vue unifiée des informations du carnet d’adresses et du fournisseur de transport. Cette approche intégrée empêche l’application cliente d’avoir à mapper les données au fournisseur approprié. Il empêche également l’utilisateur d’avoir à négocier entre plusieurs carnets d’adresses et schémas d’adressage de fournisseur de transport. Toutefois, les informations du fournisseur du magasin de messages ne sont pas unifiées et les clients qui utilisent plusieurs fournisseurs de magasins de messages sont responsables de leur gestion individuelle.
  
Les fournisseurs de services travaillent avec MAPI pour créer et envoyer des messages de la façon suivante : les messages sont créés à l’aide d’un formulaire approprié pour le type ou la classe spécifique du message. De nombreux messages sont créés avec le formulaire de note standard fourni avec le sous-système MAPI, soit par l’utilisateur d’une application cliente, soit par programmation sans interaction de l’utilisateur. Le message terminé est adressé à un ou plusieurs destinataires , un utilisateur ou un groupe d’utilisateurs désignés pour recevoir le message. Un destinataire peut ou non avoir une entrée dans un répertoire appartenant à l’un des fournisseurs de carnets d’adresses installés. Les destinataires qui ne sont pas associés à un fournisseur de carnet d’adresses installé sont appelés destinataires personnalisés ou adresses uniques. Une adresse unique peut être temporaire, ne dure que jusqu’à ce que le message soit envoyé. 
  
Lorsque l’application cliente envoie le message, le fournisseur du magasin de messages vérifie que chaque destinataire a une adresse unique et valide et que le message contient toutes les informations nécessaires à la transmission. S’il existe une question concernant un destinataire (par exemple, lorsqu’il existe plusieurs destinataires portant le même nom), un fournisseur de carnet d’adresses s’occupe de résoudre l’ambiguïté. Le message est ensuite placé dans la file d’attente sortante. 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalités et architecture MAPI](mapi-features-and-architecture.md)

