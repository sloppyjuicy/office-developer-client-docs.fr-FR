---
title: Types de fournisseurs de transport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315378"
---
# <a name="types-of-transport-providers"></a>Types de fournisseurs de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les fournisseurs de transport prennent en charge une gamme de fonctionnalités standard, telles que:
  
- Assurer une sécurité appropriée pour le système de messagerie sous-jacent.
    
- Envoi et réception de messages à partir du système de messagerie sous-jacent.
    
- En exposant les types d'adresses pris en charge par les fournisseurs de transport, le spouleur MAPI et les applications clientes peuvent les utiliser correctement.
    
- Acceptation de la remise de destinataires spécifiques.
    
De plus, MAPI prend en charge deux types de fournisseurs spécialisés pour des systèmes de messagerie spécifiques.
  
|**Type de transport**|**Fonctionnalités ajoutées**|
|:-----|:-----|
|Transport à distance  <br/> |Permet l'interopérabilité avec les clients connectés à distance.  <br/> |
|Transport TNEF  <br/> |Permet de conserver les propriétés MAPI sur les systèmes de messagerie qui ne les prennent pas en charge.  <br/> |
   
Les transports TNEF sont utilisés pour traduire les messages entre les systèmes de messagerie qui prennent en charge différents ensembles de propriétés MAPI. Les transports TNEF utilisent l'interface MAPI [ITnef: IUnknown](itnefiunknown.md) pour convertir les propriétés que le système de destination ne peut pas représenter directement dans un flux de données binaire qui peut être attaché au message. Par la suite, un autre transport TNEF peut utiliser **ITnef** pour décoder le flux de données et mettre les propriétés MAPI d'origine à la disposition des applications clientes. En outre, la prise en charge de TNEF est requise si votre transport doit prendre en charge des classes de message personnalisées. Pour plus d'informations sur l'implémentation des transports TNEF, consultez [la rubrique développement d'un fournisseur de transport compatible TNEF](developing-a-tnef-enabled-transport-provider.md).
  
Si votre fournisseur de transport n'est pas l'un de ces types, vous devrez l'implémenter avec les fonctions MAPI de base et les fonctions réseau disponibles sur votre plateforme cible.
  

