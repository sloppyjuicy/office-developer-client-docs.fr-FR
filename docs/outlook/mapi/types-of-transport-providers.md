---
title: Types de fournisseurs de transport
description: Décrit comment les fournisseurs de transport prennent en charge une gamme de fonctionnalités standard dans Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
ms.openlocfilehash: 472b7510214eee307d4554e4afe90a297bacfbd8
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894669"
---
# <a name="types-of-transport-providers"></a>Types de fournisseurs de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les fournisseurs de transport prennent en charge une gamme de fonctionnalités standard, telles que :
  
- Fourniture d’une sécurité appropriée pour le système de messagerie sous-jacent.
    
- Envoi et réception de messages à partir du système de messagerie sous-jacent.
    
- Exposition des types d’adresse pris en charge par les fournisseurs de transport afin que le spouleur MAPI et les applications clientes puissent les utiliser de manière appropriée.
    
- Acceptation de la remise pour des destinataires spécifiques.
    
En outre, MAPI prend en charge deux types de fournisseurs spécialisés pour des systèmes de messagerie spécifiques.
  
|**Type de transport**|**Ajout de fonctionnalités**|
|:-----|:-----|
|Transport à distance  <br/> |Permet l’interopérabilité avec les clients connectés à distance. |
|TNEF Transport  <br/> |Permet de conserver les propriétés MAPI sur les systèmes de messagerie qui ne les prennent pas en charge. |
   
Les transports TNEF sont utilisés pour traduire des messages entre des systèmes de messagerie qui prennent en charge différents ensembles de propriétés MAPI. Les transports TNEF utilisent l’interface [MAPI ITnef : IUnknown](itnefiunknown.md) pour convertir les propriétés que le système de destination ne peut pas représenter directement dans un flux de données binaire pouvant être attaché au message. Plus tard, un autre transport TNEF peut utiliser **ITnef** pour décoder le flux de données et rendre les propriétés MAPI d’origine disponibles pour les applications clientes. En outre, la prise en charge de TNEF est requise si votre transport doit prendre en charge les classes de messages personnalisées. Pour plus d’informations sur l’implémentation des transports TNEF, consultez [Développement d’un fournisseur de transport TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).
  
Si votre fournisseur de transport n’est pas l’un de ces types, vous devrez l’implémenter avec les fonctions MAPI de base et les fonctions réseau disponibles sur votre plateforme cible.
  

