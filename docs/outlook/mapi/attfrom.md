---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432414"
---
# <a name="attfrom"></a>attFrom

**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'attribut **attFrom** est encodé sous la forme d'une structure **TRP** qui encode le nom complet et l'adresse de messagerie de l'expéditeur, suivis du nom complet et de l'adresse de l'expéditeur, suivi de tout remplissage nécessaire. Le format de **attFrom** est le suivant: 
  
**attFrom**: _TRP-structure_ sender-Display-Name _ sender-Address _ Padding 
    
Sender-Display-Name est une chaîne terminée par un caractère null qui est complétée par un caractère null supplémentaire, si nécessaire, pour atteindre une limite de 2 octets. Le remplissage à la fin de l'encodage **attFrom** se compose de autant de caractères nuls que nécessaire pour atteindre une limite **sizeof (TRP)** . 
  
_TRP:_ **trpidOneOff** cbgrtrp CCH CB 
    
Pour l'élément **attFrom** , la structure **TRP**est toujours un encodage unique, de sorte que l'trpid du champ **TRP**-structure est toujours **trpidOneOff**. Les éléments cbgrtrp, CCH et CB correspondent aux champs restants de la structure **TRP** . 
  
Le champ cbgrtrp est calculé comme la somme de **(sizeof (TRP) \*2)**, de la longueur du nom de l'expéditeur-Display-Name par un caractère NULL avec son remplissage, et de la longueur de l'adresse de l'expéditeur-terminé par un caractère null.
  
Le champ CCH est calculé comme la longueur du nom complet terminé par un caractère NULL avec son remplissage.
  
Le champ CB est calculé comme la longueur de l'adresse de l'expéditeur-terminé par un caractère null.
  
_sender-Address:_ Address-type **:** address **' \ 0 '**
    
L'adresse de l'expéditeur est une chaîne composée de quatre parties, d'un type d'adresse, d'un signe deux-points (:), de l'adresse proprement dite et d'un caractère de fin null. Par exemple, la chaîne `fax:1-909-555-1234\0` doit être une valeur Legal sender-Address.
  

