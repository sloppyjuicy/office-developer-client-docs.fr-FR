---
title: Vue d'ensemble du fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357343"
---
# <a name="mapi-transport-provider-overview"></a>Vue d'ensemble du fournisseur de transport MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de transport gèrent la transmission et la réception des messages et implémentent la sécurité, le cas échéant. Elles prennent également en charge les tâches de prétraitement et de post-traitement nécessaires. Il existe généralement un fournisseur de transport pour chaque système de messagerie actif.
  
Les applications clientes communiquent avec le fournisseur de transport via un fournisseur de banque de messages. 
  
Les fournisseurs de transport s'inscrivent à MAPI pour gérer un ou plusieurs types d'entrées de destinataires spécifiques. Lorsqu'un message est prêt à être envoyé, MAPI doit déterminer quel fournisseur de transport doit gérer la transmission. Selon le type de destinataire, MAPI peut même appeler sur plusieurs fournisseurs de transport. Si un fournisseur de transport non disponible est le seul à pouvoir gérer le destinataire, la transmission des messages est différée jusqu'à ce qu'une connexion avec ce fournisseur puisse être rétablie.
  
Certains systèmes de messagerie sont des systèmes sécurisés; tous les utilisateurs potentiels doivent entrer un ensemble d'informations d'identification valides avant d'autoriser l'accès. MAPI empêche l'accès non autorisé à ce type de système de messagerie sécurisée en faisant en sorte que le fournisseur de transport valide les informations d'identification au moment de l'ouverture de session. 
  

