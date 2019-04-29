---
title: Vue d’ensemble de la programmation MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: d69d15f0f635c81bea30401b3a6d6e3ccf620112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408340"
---
# <a name="mapi-programming-overview"></a>Vue d’ensemble de la programmation MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette référence MAPI (Microsoft Outlook Messaging API) est conçue pour les développeurs C et C++ avec un grand nombre de besoins et d'expérience en matière de messagerie. Pour les développeurs qui souhaitent utiliser MAPI pour augmenter leurs applications qui disposent de fonctionnalités de messagerie, aucune connaissance préalable spécifique n'est requise. Vous avez besoin d'un arrière-plan dans la messagerie et du modèle COM (Component Object Model) pour utiliser MAPI afin de créer des applications ou des pilotes de groupe de travail complets pour des services de système de messagerie spécialisés.
  
Avant de commencer le travail de développement, vous devez prendre en compte les informations suivantes sur l'utilisation de MAPI, le processus d'ouverture de session et la création et la configuration des profils et des services de messagerie.
  
L'interface MAPI (Messaging Application Program Interface) est un ensemble complet de fonctions que les développeurs peuvent utiliser pour créer des applications à extension messagerie. La bibliothèque de fonctions complète est appelée MAPI. MAPI permet un contrôle total du système de messagerie sur l'ordinateur client, la création et la gestion des messages, la gestion de la boîte aux lettres client, les fournisseurs de services, etc.
  
> [!NOTE]
> L'interface MAPI étendue est identique à celle de MAPI et est simplement appelée MAPI dans la documentation MAPI. 
  
 **MAPI simple**
  
Simple MAPI fournit un ensemble de fonctions qui vous permet d'ajouter un niveau de base de fonctionnalité de messagerie aux applications basées sur Microsoft Windows.
  
> [!IMPORTANT]
> La fonction simple MAPI MAPISendMail est prise en charge par Microsoft Outlook 2013 et Microsoft Outlook 2010. D'autres fonctions MAPI simples ont été déconseillées dans Windows. 
  

