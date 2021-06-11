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
  
Une structure de flux SkipBlock est un bloc de données qui commence par un nombre entière qui spécifie la longueur de la partie restante du bloc. Cette structure de flux existe dans un [flux FieldDefinition](fielddefinition-stream-structure.md) si la définition de champ est au format PropDefV2. 
  
L’objectif d’une structure de flux SkipBlock dépend de son emplacement relatif dans une série de structures comme dans l’élément de données SkipBlocks d’un flux FieldDefinition. La série SkipBlocks doit contenir au moins une structure SkipBlock qui met fin à la série et dont l’élément de données Size est égal à 0. Si la première structure n’est pas la structure finale (autrement dit, si l’élément de données Size est supérieur à 0), Outlook suppose que la première structure spécifie le nom du champ dans Unicode (UTF-16).
  
Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre spécifié ci-dessous.
  
- Taille : DWORD (4 octets), taille, en nombre d’octets, de l’élément de données de contenu.
    
- Contenu : tableau de BYTE. Le nombre de ce tableau est égal à l’élément de données Size. La signification de l’élément de données Content dépend de l’emplacement de la structure SkipBlock dans la série et de la version de Outlook. Si la première structure SkipBlock n’est pas la structure de fin, Outlook considère la première structure SkipBlock comme la structure de flux [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) qui spécifie le nom du champ dans Unicode. 
    
## <a name="see-also"></a>Voir aussi



[Outlook Éléments et champs](outlook-items-and-fields.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
  
[Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

