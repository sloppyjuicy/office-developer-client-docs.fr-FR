---
title: Vue d'ensemble de la programmation MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: bd9cdd9119f94e1f7684be34e1b4ef6fb40ab2bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576504"
---
# <a name="mapi-programming-overview"></a>Vue d'ensemble de la programmation MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ce guide de référence de Microsoft Outlook MAPI (Messaging API) est écrit pour C et développeurs C++ avec une variété de besoins et expérience avec la messagerie. Pour les développeurs qui souhaitent utiliser MAPI pour améliorer leurs applications qui ont des fonctionnalités de messagerie, sans connaissances préalables spécifique est requis. Vous avez besoin d’un arrière-plan dans la messagerie et le composant COM (Object Model) à utiliser MAPI pour créer des applications de groupe de travail à grande échelle ou pilotes pour les services de système de messagerie spécialisés.
  
Avant de commencer le travail de développement, vous devez tenir compte les informations suivantes sur l’utilisation de MAPI, le processus d’ouverture de session, et comment les profils et les services de messagerie sont créés et configurés.
  
Le programme Interface MAPI (Messaging Application) est un ensemble complet de fonctions qui permet aux développeurs de créer des applications à extension messagerie. La bibliothèque de fonctions complète est appelée MAPI. MAPI permet de contrôler le système de messagerie sur l’ordinateur client, la création et la gestion des messages, de gestion de la boîte aux lettres cliente, fournisseurs de services et ainsi de suite.
  
> [!NOTE]
> Interface MAPI étendue est identique à MAPI et est simplement appelé MAPI dans la documentation de MAPI. 
  
 **MAPI simple**
  
MAPI simple fournit un jeu de fonctions qui vous permet d’ajouter un niveau de base de la messagerie de fonctionnalités aux applications Microsoft Windows.
  
> [!IMPORTANT]
> La fonction MAPI Simple MAPISendMail est pris en charge par Microsoft Outlook 2013 et Microsoft Outlook 2010. Autres fonctions de l’interface Simple MAPI ont été déconseillées dans Windows. 
  

