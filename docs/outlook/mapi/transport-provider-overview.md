---
title: Vue d’ensemble du fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 22b9da0cfe70cf499cc6f3a699eabe4aaee25b0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787389"
---
# <a name="transport-provider-overview"></a>Vue d’ensemble du fournisseur de transport

  
  
**S’applique à**: Outlook 
  
Un fournisseur de transport est une bibliothèque de liens dynamiques (DLL) qui joue le rôle d’intermédiaire entre le sous-système MAPI et un ou plusieurs systèmes de messagerie sous-jacent. Un système de messagerie est un mécanisme spécifique à laquelle les messages sont envoyés et reçus. Quelques exemples de systèmes de messagerie sont les suivants :
  
- Un système de fichiers réseau partagé que le fournisseur de transport écrit les messages directement.
    
- Une interface réseau TCP/IP par le fournisseur de transport pour se connecter à un serveur de messagerie.
    
- Un service en ligne que les utilisateurs se connectent à.
    
- Un hôte de messagerie ou office automation système.
    
- Un ensemble d’appels de procédure distante à un serveur de messagerie.
    
- Tout ce qui peut être utilisé pour transférer des données à partir d’un ordinateur à un autre.
    
Un DLL du fournisseur de transport doit être conforme à l’interface spécifiée par MAPI. En tant que développeur de fournisseur de transport, vous allez implémenter cette interface en termes de la fonctionnalité présente dans le système de messagerie.
  

