---
title: Structure de flux SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435543"
---
# <a name="skipblock-stream-structure"></a>Structure de flux SkipBlock

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une structure de flux SkipBlock est un bloc de données qui commence par un entier qui spécifie la longueur de la partie restante du bloc. Cette structure de flux existe dans un flux [FieldDefinition](fielddefinition-stream-structure.md) si la définition de champ est au format PropDefV2. 
  
L'objectif d'une structure de flux SkipBlock dépend de son emplacement relatif dans une série de structures similaires dans l'élément de données SkipBlocks d'un flux de FieldDefinition. La série SkipBlocks doit contenir au moins une structure SkipBlock qui termine la série et dont l'élément de données de taille est égal à 0. Si la première structure n'est pas la structure de terminaison (autrement dit, l'élément de données de taille est supérieur à 0), Outlook suppose que la première structure spécifie le nom du champ en Unicode (UTF-16).
  
Les éléments de données dans ce flux sont stockés dans l'ordre d'octet Little-endian, immédiatement suivant l'ordre indiqué ci-dessous.
  
- Size: DWORD (4 octets), taille, en nombre d'octets, de l'élément de données de contenu.
    
- Content: tableau d'octets. Le nombre de ce tableau est égal à l'élément de données Size. La signification de l'élément de données de contenu dépend de l'emplacement de la structure SkipBlock dans la série et de la version d'Outlook. Si la première structure SkipBlock n'est pas la structure de terminaison, Outlook considère la première structure SkipBlock comme la structure de flux de [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) qui spécifie le nom de champ en Unicode. 
    
## <a name="see-also"></a>Voir aussi



[Éléments et champs Outlook](outlook-items-and-fields.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
  
[Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

