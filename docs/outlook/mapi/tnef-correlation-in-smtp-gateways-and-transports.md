---
title: Corrélation TNEF dans les transports et passerelles SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8192646007e8935a750a70e46b8210eebbc353f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578534"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Corrélation TNEF dans les transports et passerelles SMTP

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Systèmes, celles qui utilisent le protocole SMTP, utilisez la valeur de l’en-tête SMTP MessageID et la propriété **PR_TNEF_CORRELATION_KEY** pour implémenter la corrélation TNEF en fonction de passerelles et des transports qui se connectent à internet. 
  
La valeur de l’en-tête MessageID du message sortant doit être copiée dans la propriété **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) et codée dans l’attribut [attMAPIProps](attmapiprops.md) de l’objet stream TNEF. Notez que **PR_TNEF_CORRELATION_KEY** est une propriété binaire, tandis que l’ID du message est une chaîne ; le terminateur null doit être inclus dans la copie et la comparaison. 
  
Cette technique est utilisée par tous les logiciels Microsoft qui connecte des systèmes de messagerie basé sur MAPI à Internet, telle que Microsoft Exchange Server. Cette technique doit être utilisée par les passerelles SMTP et les transports de se connecter aux systèmes qui prennent en charge des clients MAPI afin d’optimiser l’interopérabilité.
  

