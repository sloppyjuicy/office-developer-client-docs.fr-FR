---
title: Corrélation TNEF dans les passerelles et transports X.400
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e08f16ff60a282f1be3adf93d858471e38d19957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406373"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>Corrélation TNEF dans les passerelles et transports X.400

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les passerelles et les transports qui se connectent à des systèmes X.400 utilisent la valeur de l’attribut IM_THIS_IPM X.400 et de l’attribut **TNEF attMessageID** pour implémenter la corrélation TNEF. 
  
La valeur de l IM_THIS_IPM du message sortant est copiée dans **attMessageID** dans le flux TNEF. L IM_THIS_IPM X.400 est généralement une chaîne, tandis que l’attribut **TNEF attMessageID** est une chaîne de chiffres hexadécimaux représentant une valeur binaire. Par conséquent, chaque caractère de l’attribut IM_THIS_IPM X.400, y compris le caractère null de fin, doit être converti en chaîne hexadécimale à 2 caractères représentant la valeur ASCII de ce caractère. Par exemple, si l’IM_THIS_IPM X.400 est la chaîne suivante : 
  
3030322D3030312D305337533A3A3936303631312D31353337303030
  
la valeur **d’attMessageID** serait alors la séquence de chiffres hexadécimal suivante : 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
Cette technique est utilisée par le Microsoft Exchange Server connecteur X.400. Cette technique doit être utilisée par les passerelles et les transports X.400 qui se connectent à Microsoft Exchange Server afin d’optimiser l’interopérabilité.
  
Pour une meilleure compatibilité avec les logiciels Microsoft futurs et présents, l’attribut IM_THIS_IPM X.400 doit également être copié dans la propriété **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)). Toutefois, comme **PR_TNEF_CORRELATION_KEY** est une propriété binaire, aucune traduction en chaîne hexadécimale n’est nécessaire. 
  

