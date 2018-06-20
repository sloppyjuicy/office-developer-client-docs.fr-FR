---
title: Types de fournisseurs de Transport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4a0ab660b8df2fb32f21f9bc93932a9187c37b7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787390"
---
# <a name="types-of-transport-providers"></a>Types de fournisseurs de Transport

  
  
**S’applique à**: Outlook 
  
Tous les fournisseurs de transport prennent en charge une variété de fonctionnalités standards, telles que :
  
- Fournir une sécurité appropriée pour le système de messagerie sous-jacent.
    
- Envoi et réception de messages à partir du système de messagerie sous-jacent.
    
- Exposer les types d’adresses les fournisseurs de transport prennent en charge le spouleur MAPI et les applications clientes peuvent les utiliser correctement.
    
- Accepter la livraison pour des destinataires spécifiques.
    
En outre, MAPI prend en charge deux types de fournisseurs spécialisés pour les systèmes de messagerie spécifiques.
  
|**Type de transport**|**Ajout de fonctionnalités**|
|:-----|:-----|
|Transport à distance  <br/> |Permet l’interopérabilité avec les clients connectés à distance.  <br/> |
|Transport TNEF  <br/> |Permet d’être perdues sur qui ne prennent pas en charge les systèmes de messagerie des propriétés MAPI.  <br/> |
   
Transports TNEF sont utilisés pour la traduction des messages entre les systèmes de messagerie qui prennent en charge différentes propriétés MAPI. Transports TNEF utilisent l’interface MAPI [ITnef : IUnknown](itnefiunknown.md) interface pour convertir des propriétés représentant le système de destination ne peut pas directement dans un flux de données binaires qui peut être joint au message. Ultérieurement, un autre transport TNEF peut utiliser **ITnef** pour décoder le flux de données et de rendre les propriétés MAPI d’origine disponibles pour les applications clientes. En outre, la prise en charge TNEF est requis si votre transport doit prendre en charge des classes de message personnalisées. Pour plus d’informations sur l’implémentation des transports TNEF, voir [développement d’un fournisseur de Transport TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).
  
Si votre fournisseur de transport n’est pas un de ces types, vous devrez implémenter avec les fonctions de base MAPI et les fonctions réseau disponibles sur votre plateforme cible.
  

