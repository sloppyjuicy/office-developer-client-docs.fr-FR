---
title: Vue d’ensemble de la programmation MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: be3cc0c76efc93b32cb0a939065de88ae5217fdd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567143"
---
# <a name="mapi-programming-overview"></a>Vue d’ensemble de la programmation MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette référence MAPI (Microsoft Outlook Messaging API) est écrite pour les développeurs C et C++ ayant divers besoins et expériences en matière de messagerie. Pour les développeurs qui souhaitent utiliser MAPI pour enrichir leurs applications qui disposent de fonctionnalités de messagerie, aucune connaissance préalable spécifique n’est requise. Vous avez besoin d’une expérience en messagerie et du modèle objet composant (COM) pour utiliser MAPI afin de créer des applications de groupe de travail à grande échelle ou des pilotes pour des services système de messagerie spécialisés.
  
Avant de commencer le travail de développement, vous devez prendre en compte les informations suivantes sur l’utilisation de MAPI, le processus d’accès et la façon dont les profils et les services de message sont créés et configurés.
  
MapI (Messaging Application Program Interface) est un ensemble étendu de fonctions que les développeurs peuvent utiliser pour créer des applications à messagerie. La bibliothèque de fonctions complète est appelée MAPI. MAPI permet un contrôle total du système de messagerie sur l’ordinateur client, la création et la gestion des messages, la gestion de la boîte aux lettres cliente, les fournisseurs de services, etc.
  
> [!NOTE]
> MapI étendu est identique à MAPI et est simplement appelé MAPI dans la documentation MAPI. 
  
 **MAPI simple**
  
MapI simple fournit un ensemble de fonctions qui vous permet d’ajouter un niveau de base de fonctionnalité de messagerie aux applications microsoft Windows base.
  
> [!IMPORTANT]
> La fonction MAPISendMail simple est prise en charge par les Microsoft Outlook 2013 et Microsoft Outlook 2010. D’autres fonctions MAPI simples ont été Windows. 
  

