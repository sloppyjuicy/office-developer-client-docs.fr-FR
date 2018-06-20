---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c7c0d1df32a0ad6359fad20128a6a1e3dd225143
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782971"
---
# <a name="attfrom"></a>attFrom

**S’applique à**: Outlook 
  
L’attribut **attFrom** est codé en une structure **TRP** qui encode l’adresse d’e-mail et le nom complet de l’expéditeur, suivi par le nom complet et l’adresse de l’expéditeur, suivi par n’importe quel remplissage nécessaire. Le format de **attFrom** est la suivante : 
  
**attFrom**: remplissage d’une _structure-TRP_ _ expéditeur nom d’affichage adresse d’expéditeur _ 
    
Le nom complet l’expéditeur est une chaîne qui est remplie par un caractère null supplémentaire, si nécessaire, pour atteindre une limite de 2 octets. Le remplissage à la fin de la méthode de codage **attFrom** se compose de caractères de null autant que nécessaire pour atteindre une limite **sizeof(TRP)** . 
  
_TRP-structure :_ **trpidOneOff** cbgrtrp cch cb 
    
Pour l’élément **attFrom** , la **TRP**-structure est toujours un uniques codage, donc la trpid désactive le **TRP**-champ de la structure est toujours **trpidOneOff**. Cbgrtrp, cch, les éléments cb correspondent aux champs restants de la structure **TRP** . 
  
Le champ cbgrtrp est calculé comme la somme des **(sizeof(TRP) \*2)**, la longueur de caractère nul-affichage-nom de l’expéditeur avec son remplissage et la longueur de l’adresse expéditeur terminée.
  
Le champ cch est calculé en tant que la longueur du caractère nul-nom d’affichage avec son remplissage.
  
Le champ cb est calculé en tant que la longueur de l’adresse expéditeur terminée.
  
_-adresse de l’expéditeur :_ type d’adresse **:** adresse **'\0'**
    
L’adresse de l’expéditeur est une chaîne qui se compose de quatre parties, le type d’adresse, littéral (deux-points), l’adresse lui-même et un caractère null de fin. Par exemple, la chaîne `fax:1-909-555-1234\0` est une valeur de l’adresse de l’expéditeur juridique.
  

