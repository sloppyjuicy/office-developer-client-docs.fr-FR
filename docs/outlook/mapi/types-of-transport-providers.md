---
title: Types de fournisseurs de transport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406163"
---
# <a name="types-of-transport-providers"></a>Types de fournisseurs de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les fournisseurs de transport supportent une gamme de fonctionnalités standard, telles que :
  
- Assurer une sécurité appropriée pour le système de messagerie sous-jacent.
    
- Envoi et réception de messages à partir du système de messagerie sous-jacent.
    
- Exposition des types d’adresses que les fournisseurs de transport prise en charge afin que lepooler MAPI et les applications clientes peuvent les utiliser correctement.
    
- Accepter la remise pour des destinataires spécifiques.
    
En outre, MAPI prend en charge deux types spécialisés de fournisseurs pour des systèmes de messagerie spécifiques.
  
|**Type de transport**|**Fonctionnalités ajoutées**|
|:-----|:-----|
|Transport à distance  <br/> |Active l’interopérabilité avec les clients connectés à distance.  <br/> |
|TNEF Transport  <br/> |Permet de conserver les propriétés MAPI sur les systèmes de messagerie qui ne les prisent pas en charge.  <br/> |
   
Les transports TNEF sont utilisés pour traduire des messages entre des systèmes de messagerie qui utilisent différents ensembles de propriétés MAPI. Les transports TNEF utilisent l’interface MAPI [ITnef : IUnknown](itnefiunknown.md) pour convertir les propriétés que le système de destination ne peut pas représenter directement en un flux de données binaires qui peut être joint au message. Par la suite, un autre transport TNEF peut utiliser **ITnef** pour décoder le flux de données et rendre les propriétés MAPI d’origine disponibles pour les applications clientes. En outre, la prise en charge du TNEF est requise si votre transport doit prendre en charge des classes de message personnalisées. Pour plus d’informations sur l’implémentation des transports TNEF, voir [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
  
Si votre fournisseur de transport n’est pas de ce type, vous devez l’implémenter avec les fonctions MAPI de base et les fonctions réseau disponibles sur votre plateforme cible.
  

