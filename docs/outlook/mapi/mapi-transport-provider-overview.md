---
title: Vue d’ensemble du fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
ms.openlocfilehash: f376b717f2da90bb9a28913bdf6be71fd6338383
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377749"
---
# <a name="mapi-transport-provider-overview"></a>Vue d’ensemble du fournisseur de transport MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de transport gèrent la transmission et la réception des messages et implémentent la sécurité, si nécessaire. Ils s’occupent également de toutes les tâches de prétraitage et de post-traitement nécessaires. Il existe généralement un fournisseur de transport pour chaque système de messagerie actif.
  
Les applications clientes communiquent avec le fournisseur de transport via un fournisseur de magasins de messages. 
  
Les fournisseurs de transport s’inscrivent auprès de MAPI pour gérer un ou plusieurs types particuliers d’entrées de destinataire. Lorsqu’un message est prêt à être envoyé, MAPI doit déterminer le fournisseur de transport qui doit gérer la transmission. Selon le type de destinataire, MAPI peut même appeler plusieurs fournisseurs de transport. Si un fournisseur de transport indisponible est le seul à pouvoir gérer le destinataire, la transmission du message est différée jusqu’à ce qu’une connexion avec ce fournisseur puisse être rétablie.
  
Certains systèmes de messagerie sont des systèmes sécurisés ; Tous les utilisateurs potentiels doivent entrer un ensemble d’informations d’identification valides avant d’autoriser l’accès. MAPI empêche l’accès non autorisé à ces systèmes de messagerie sécurisés en faisant valider les informations d’identification par le fournisseur de transport au moment de l’connexion. 
  

