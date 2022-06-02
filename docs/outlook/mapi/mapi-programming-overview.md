---
title: Vue d’ensemble de la programmation MAPI
description: Cette référence MAPI (Microsoft Outlook Messaging API) est écrite pour les développeurs C et C++ avec une variété de besoins et d’expérience en matière de messagerie.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
ms.openlocfilehash: 6230cb294e5a7cb0e976f9051ce64a0fd93973dc
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828205"
---
# <a name="mapi-programming-overview"></a>Vue d’ensemble de la programmation MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette référence MAPI (Microsoft Outlook Messaging API) est écrite pour les développeurs C et C++ avec une variété de besoins et d’expérience en matière de messagerie. Pour les développeurs qui souhaitent utiliser MAPI pour augmenter leurs applications dotées de fonctionnalités de messagerie, aucune connaissance requise spécifique n’est requise. Vous avez besoin d’une formation en messagerie et du modèle d’objet de composant (COM) pour utiliser MAPI afin de créer des applications ou des pilotes de groupe de travail à grande échelle pour les services de système de messagerie spécialisés.
  
Avant de commencer le travail de développement, vous devez prendre en compte les informations suivantes sur l’utilisation de MAPI, le processus d’ouverture de session et la façon dont les profils et les services de messages sont créés et configurés.
  
L’interface mapi (Messaging Application Program Interface) est un ensemble complet de fonctions que les développeurs peuvent utiliser pour créer des applications à extension messagerie. La bibliothèque de fonctions complète est appelée MAPI. MAPI permet un contrôle total sur le système de messagerie sur l’ordinateur client, la création et la gestion des messages, la gestion de la boîte aux lettres du client, les fournisseurs de services, et ainsi de suite.
  
> [!NOTE]
> MapI étendu est identique à MAPI et est simplement appelé MAPI dans la documentation MAPI. 
  
 **MAPI simple**
  
Simple MAPI fournit un ensemble de fonctions qui vous permet d’ajouter un niveau de base de fonctionnalités de messagerie aux applications basées sur Microsoft Windows.
  
> [!IMPORTANT]
> La fonction MAPI SIMPLE MAPI MAPISendMail est prise en charge par Microsoft Outlook 2013 et Microsoft Outlook 2010. D’autres fonctions MAPI simples ont été déconseillées dans Windows. 
  

