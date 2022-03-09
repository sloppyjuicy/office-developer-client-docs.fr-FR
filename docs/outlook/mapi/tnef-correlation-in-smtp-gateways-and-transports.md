---
title: Corrélation TNEF dans les passerelles et transports SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
ms.openlocfilehash: d62dbe3c6ed470c771c4164380788853bbc05d64
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380969"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Corrélation TNEF dans les passerelles et transports SMTP

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les passerelles et les transports qui se connectent à des systèmes Internet, ceux qui utilisent SMTP, utilisent la valeur de l’en-tête SMTP MessageID et de la propriété **PR_TNEF_CORRELATION_KEY** pour implémenter la corrélation TNEF. 
  
La valeur de l’en-tête MessageID du message sortant doit être copiée dans la propriété **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) et codée dans l’attribut [attMAPIProps](attmapiprops.md) du flux TNEF. Notez **que PR_TNEF_CORRELATION_KEY** est une propriété binaire, tandis que MessageID est une chaîne ; le terminateur null doit être inclus dans la copie et dans la comparaison. 
  
Cette technique est utilisée par tous les logiciels Microsoft qui connectent des systèmes de messagerie MAPI à Internet, tels que Microsoft Exchange Server. Cette technique doit être utilisée par les passerelles et les transports SMTP qui se connectent aux systèmes qui prendre en charge les clients MAPI afin d’optimiser l’interopérabilité.
  

