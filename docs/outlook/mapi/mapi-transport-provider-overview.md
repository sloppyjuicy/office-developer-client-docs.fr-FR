---
title: Vue d’ensemble du fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 42c41bd3f09a62c940a9b8b598a7adcd7dfccf08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556097"
---
# <a name="mapi-transport-provider-overview"></a>Vue d’ensemble du fournisseur de transport MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de transport gèrent la transmission et la réception des messages et implémentent la sécurité, si nécessaire. Ils s’occupent également de toutes les tâches de prétraitage et de post-traitement nécessaires. Il existe généralement un fournisseur de transport pour chaque système de messagerie actif.
  
Les applications clientes communiquent avec le fournisseur de transport via un fournisseur de magasins de messages. 
  
Les fournisseurs de transport s’inscrivent auprès de MAPI pour gérer un ou plusieurs types particuliers d’entrées de destinataire. Lorsqu’un message est prêt à être envoyé, MAPI doit déterminer le fournisseur de transport qui doit gérer la transmission. Selon le type de destinataire, MAPI peut même appeler plusieurs fournisseurs de transport. Si un fournisseur de transport indisponible est le seul à pouvoir gérer le destinataire, la transmission du message est reportée jusqu’à ce qu’une connexion avec ce fournisseur puisse être rétablie.
  
Certains systèmes de messagerie sont des systèmes sécurisés ; Tous les utilisateurs potentiels doivent entrer un ensemble d’informations d’identification valides avant d’autoriser l’accès. MAPI empêche l’accès non autorisé à ces systèmes de messagerie sécurisés en faisant valider les informations d’identification par le fournisseur de transport au moment de l’connexion. 
  

