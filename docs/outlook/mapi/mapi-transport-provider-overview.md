---
title: Vue d’ensemble du fournisseur de Transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 11cd1040bb228d789248a89184572b87cd1688ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784728"
---
# <a name="mapi-transport-provider-overview"></a>Vue d’ensemble du fournisseur de Transport MAPI

  
  
**S’applique à**: Outlook 
  
Fournisseurs de transport gérer la réception et transmission de message et implémentent la sécurité, si nécessaire. Ils s’occupent aussi de prétraitement nécessaires et les tâches de post-traitement. Il est généralement un fournisseur de transport pour chaque système de messagerie active.
  
Les applications clientes communiquent avec le fournisseur de transport via un fournisseur de magasin de message. 
  
Fournisseurs de transport inscrire MAPI pour gérer un ou plusieurs types particuliers d’entrées de destinataire. Lorsqu’un message est prêt à être envoyé, MAPI doit déterminer le fournisseur de transport doit gérer la transmission. Selon le type de destinataire, MAPI peut être appelés même plus d’un fournisseur de transport. Si un fournisseur de transport indisponible est le seul qui peut gérer le destinataire, la transmission de message sera différée jusqu'à ce qu’une connexion avec ce fournisseur peut être rétablie.
  
Certains systèmes de messagerie sont des systèmes d’informations sécurisé ; tous les utilisateurs potentiels doivent entrer un ensemble d’informations d’identification valides avant de pouvoir accéder. MAPI empêche l’accès non autorisé à des systèmes de messagerie sécurisées organisez le fournisseur de transport de valider les informations d’identification au moment de l’ouverture de session. 
  

