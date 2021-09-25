---
title: Vue d’ensemble du fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f189ed78d7feb1714fa2a04bf29403c6d33773af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609319"
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
  

