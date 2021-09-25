---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a3b149b3b9a28cdf4043ace5da667b18729a077d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572101"
---
# <a name="attfrom"></a>attFrom

**S’applique à** : Outlook 2013 | Outlook 2016 
  
**L’attribut attFrom** est codé en tant que structure **TRP** qui encode le nom complet et l’adresse e-mail de l’expéditeur, suivi du nom complet et de l’adresse de l’expéditeur, puis de tout remplissage nécessaire. Le format de **attFrom** est le suivant : 
  
**attFrom**: _TRP-structure_ sender-display-name _ sender-address _ padding 
    
Le nom complet de l’expéditeur est une chaîne terminée par un caractère null qui est ajoutée avec un caractère null supplémentaire, si nécessaire, pour atteindre une limite de 2 byte. Le remplissage à la fin du codage **attFrom** se compose d’autant de caractères null que nécessaire pour atteindre une limite **sizeof(TRP).** 
  
_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb 
    
Pour l’élément **attFrom,** la structure **TRP** est toujours un codage unique, donc le trpid hors du champ **TRP**-structure est **toujours trpidOneOff**. Les éléments cbgrtrp, cch et cb correspondent aux champs restants de la structure **TRP.** 
  
Le champ cbgrtrp est calculé comme la somme **de (sizeof(TRP) \* 2),** la longueur du nom complet de l’expéditeur terminé par null avec son remplissage et la longueur de l’adresse-expéditeur terminée par null.
  
Le champ cch est calculé comme la longueur du nom complet terminé par null avec son remplissage.
  
Le champ cb est calculé comme la longueur de l’adresse-expéditeur terminée par null.
  
_sender-address:_ address-type **:** address **'\0'**
    
L’adresse de l’expéditeur est une chaîne composée de quatre parties: le type d’adresse, un deux-points littéral (:), l’adresse elle-même et un caractère null de fin. Par exemple, la chaîne `fax:1-909-555-1234\0` serait une valeur d’adresse d’expéditeur légale.
  

