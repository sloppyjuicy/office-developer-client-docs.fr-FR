---
title: Corrélation TNEF dans les passerelles et transports SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413667"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Corrélation TNEF dans les passerelles et transports SMTP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les passerelles et les transports qui se connectent à des systèmes Internet, ceux qui utilisent SMTP, utilisent la valeur de l’en-tête SMTP MessageID et de la propriété **PR_TNEF_CORRELATION_KEY** pour implémenter la corrélation TNEF. 
  
La valeur de l’en-tête MessageID du message sortant doit être copiée dans la propriété **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) et codée dans l’attribut [attMAPIProps](attmapiprops.md) du flux TNEF. Notez **que PR_TNEF_CORRELATION_KEY** est une propriété binaire, tandis que MessageID est une chaîne ; le terminateur null doit être inclus dans la copie et dans la comparaison. 
  
Cette technique est utilisée par tous les logiciels Microsoft qui connectent des systèmes de messagerie MAPI à Internet, tels que Microsoft Exchange Server. Cette technique doit être utilisée par les passerelles smTP et les transports qui se connectent aux systèmes qui prendre en charge les clients MAPI afin d’optimiser l’interopérabilité.
  

