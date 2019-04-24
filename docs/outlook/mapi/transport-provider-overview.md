---
title: Vue d'ensemble du fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356636"
---
# <a name="transport-provider-overview"></a>Vue d'ensemble du fournisseur de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de transport est une bibliothèque de liens dynamiques (DLL) qui se comporte comme un intermédiaire entre le sous-système MAPI et un ou plusieurs systèmes de messagerie sous-jacents. Un système de messagerie est un mécanisme spécifique par lequel les messages sont envoyés et reçus. Voici quelques exemples de systèmes de messagerie:
  
- Système de fichiers réseau partagé que le fournisseur de transport écrit les messages directement.
    
- Une interface réseau TCP/IP que le fournisseur de transport utilise pour se connecter à un serveur de messagerie.
    
- Service en ligne auquel se connectent les utilisateurs.
    
- Un système de messagerie ou d'automatisation Office basé sur l'hôte.
    
- Un ensemble d'appels de procédure distante à un serveur de messagerie.
    
- Tout élément pouvant être utilisé pour transférer des données d'un ordinateur à un autre.
    
Une DLL de fournisseur de transport doit être conforme à l'interface spécifiée par MAPI. En tant que développeur de fournisseurs de transport, vous implémenterez cette interface en termes de fonctionnalités présentes dans le système de messagerie.
  

