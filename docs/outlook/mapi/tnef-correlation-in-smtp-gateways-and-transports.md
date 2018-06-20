---
title: Corrélation TNEF dans les passerelles SMTP et des Transports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ec1d826ee2b3b46685a2c03dfaf45d2843869cc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787359"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Corrélation TNEF dans les passerelles SMTP et des Transports

  
  
**S’applique à**: Outlook 
  
Systèmes, celles qui utilisent le protocole SMTP, utilisez la valeur de l’en-tête SMTP MessageID et la propriété **PR_TNEF_CORRELATION_KEY** pour implémenter la corrélation TNEF en fonction de passerelles et des transports qui se connectent à internet. 
  
La valeur de l’en-tête MessageID du message sortant doit être copiée dans la propriété **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) et codée dans l’attribut [attMAPIProps](attmapiprops.md) de l’objet stream TNEF. Notez que **PR_TNEF_CORRELATION_KEY** est une propriété binaire, tandis que l’ID du message est une chaîne ; le terminateur null doit être inclus dans la copie et la comparaison. 
  
Cette technique est utilisée par tous les logiciels Microsoft qui connecte des systèmes de messagerie basé sur MAPI à Internet, telle que Microsoft Exchange Server. Cette technique doit être utilisée par les passerelles SMTP et les transports de se connecter aux systèmes qui prennent en charge des clients MAPI afin d’optimiser l’interopérabilité.
  

