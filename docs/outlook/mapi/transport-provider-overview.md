---
title: Vue d’ensemble du fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
ms.openlocfilehash: 115e6f2e647dd3359a7aa718b763834fca245f08
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370217"
---
# <a name="transport-provider-overview"></a>Vue d’ensemble du fournisseur de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de transport est une bibliothèque de liens dynamiques (DLL) qui agit comme un intermédiaire entre le sous-système MAPI et un ou plusieurs systèmes de messagerie sous-jacents. Un système de messagerie est un mécanisme spécifique par lequel les messages sont envoyés et reçus. Voici quelques exemples de systèmes de messagerie :
  
- Un système de fichiers réseau partagé dans qui le fournisseur de transport écrit directement des messages.
    
- Interface réseau TCP/IP que le fournisseur de transport utilise pour se connecter à un serveur de messagerie.
    
- Service en ligne à qui les utilisateurs se connectent.
    
- Une messagerie basée sur l’hôte ou un système d’automatisation Office.
    
- Ensemble d’appels de procédure distante vers un serveur de messagerie.
    
- Tout ce qui peut être utilisé pour transférer des données d’un ordinateur à un autre.
    
Une DLL de fournisseur de transport doit être conforme à l’interface spécifiée par MAPI. En tant que développeur de fournisseurs de transport, vous implémentez cette interface en termes de fonctionnalités présentes dans le système de messagerie.
  

