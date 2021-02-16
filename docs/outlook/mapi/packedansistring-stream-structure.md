---
title: PackedAnsiString Stream Structure
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404504"
---
# <a name="packedansistring-stream-structure"></a>PackedAnsiString Stream Structure

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La structure de flux PackedAnsiString contient une représentation ANSI d’une chaîne, basée sur la page de code ANSI de l’ordinateur sur lequel Microsoft Outlook est en cours d’exécution. Cette chaîne n’est pas terminée par un caractère null. Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre indiqué ci-dessous. Les éléments de données réels qui existent dépendent de la longueur de la chaîne dans la représentation ANSI.
  
- Pour une chaîne dont la représentation ANSI contient moins de 255 octets, les éléments de données sont les suivants :
    
  - Longueur : BYTE (1 octet), longueur, en nombre d’octets, de la représentation ANSI de la chaîne.
    
  - Characters: An array of CHAR. Le nombre de ce tableau est égal à l’élément de données Length. Les données du tableau sont la représentation ANSI de la chaîne.
    
- Pour une chaîne dont la représentation ANSI contient entre 255 et 65 535 octets, les éléments de données sont les suivants :
    
  - Préfixe : BYTE (1 byte), la valeur de 255 (0xff).
    
  - Longueur : WORD (2 octets), longueur, en nombre d’octets, de la représentation ANSI de la chaîne.
    
  - Characters: An array of CHAR. Le nombre de ce tableau est égal à l’élément de données Length. Les données du tableau sont la représentation ANSI de la chaîne.
    
## <a name="see-also"></a>Voir aussi



[Éléments et champs Outlook](outlook-items-and-fields.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)

