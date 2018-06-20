---
title: Section de formulaire Configuration de fichier [propriétés]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f582322c8ba2ffa0369792e531adf1ec4ccb3e28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783361"
---
# <a name="form-configuration-file-properties-section"></a>Section de formulaire Configuration de fichier [propriétés]

  
  
**S’applique à**: Outlook 
  
La section **[propriétés]** répertorie l’ensemble complet des propriétés qui utilise le formulaire et qui publie ; Autrement dit, les propriétés qu’il crée dans ses messages personnalisés que MAPI client applications peuvent utiliser lors de l’affichage des colonnes, le filtrage des tables de contenu, configuration des dossiers de résultats de recherche et ainsi de suite. Chaque entrée de liste de cette propriété fait référence suivante **[propriété.** _chaîne_ section **]** comme suit indiqué. 
  
 **[Propriétés]**
  
 **Propriété.** _chaîne_ =  _chaîne_
  
Le format d’un [ **propriété.** _chaîne_] section est la suivante : 
  
 **[Property.** _chaîne_ **]**
  
 **Type de** =  _entier_
  
 **NmidPropset** =  _guid_
  
 **NmidString** =  _chaîne_
  
 **Touche** =  _entier_
  
 **DisplayName** =  _chaîne_
  
 **Indicateurs** =  _entier_
  
 **SpecialType** = 0 | 1 
  
 **Enum1** =  _chaîne_
  
Chaque **[propriété.** _chaîne_ section **]** décrit une propriété unique. L’entrée de **Type** Spécifie le type de propriété MAPI, par exemple 3 (PT_I4), de la propriété. L’entrée **NmidPropset** est facultative ; avec l’entrée **NmidString** ou la **touche** entrée, l’entrée **NmidPropset** donne le nom de la propriété. **NmidString** attribue le nom de la propriété, tandis que la **touche** donne l’identificateur de la propriété. **NmidString** et **nécessite** s’excluent mutuellement. 
  
Si set, **NmidPropset** doit contenir le nom du jeu de propriétés ; Si absent, **NmidPropset** est défini sur une valeur par défaut en fonction de la règle suivante : si la **touche** est présente et que sa valeur est inférieure à 0 x 8000, **NmidPropset** est défini sur PS_MAPI. Si la valeur de la **touche** est définie à un nombre entier supérieure à 0 x 8000, ou si elle est absente, **NmidPropset** est définie sur PS_PUBLIC_STRINGS. 
  
L’entrée **DisplayName** contient l’étiquette de la propriété. L’entrée **SpecialType** , si présent et différente de zéro indique que cette propriété est une propriété spéciale. À présent, le type de propriété spéciale uniquement défini est **SpecialType** = 1, ce qui indique les propriétés de la chaîne énumérée. Si **SpecialType** est défini sur 1, l’entrée **Enum1** fait référence à la **[Enum1.** _chaîne_ section **]** . 
  
Voici un exemple d’une section **[propriétés]** et **[Propriétés.** _chaîne_ section **]** . 
  
```cpp
[Properties]
Property.1 = Fire Hazard
Property.2 = Safe
[Property.Fire Hazard]
Type = 1
NmidPropSet = {E47F4480-8400-101B-934D-04021C007002]
NmidString = FireHazard
DisplayName = Fire Hazard
SpecialType = 1
Enum1 = HazardEnum

```

L’entrée **Enum1** dans les références d’exemple précédent d’un **[Enum1.** _chaîne_ section **]** décrivant une énumération d’un type particulier. Cette énumération associe la première propriété de la **[propriété.** _chaîne_ section **]** avec une propriété entière, appelé l’index. Cette énumération contient également une liste de la paire d’affichage-index peut prendre les valeurs possibles. Spécification d’un type de propriété pour l’énumération n’est pas nécessaire, car, par définition une entrée **Enum1** a toujours le type PT_I4. Le format de la **[Enum1.** _chaîne_ section **]** est : 
  
 **[Enum1.** _chaîne_ **]**
  
 **NmidPropset** =  _guid_
  
 **NmidString** =  _chaîne_
  
 **Touche** =  _entier_
  
 **EnumCount** =  _entier_
  
 **Val.** _entier_ **. Affichage** =  _chaîne_
  
 **Val.** _entier_ **. Index** =  _entier_
  
Voici un exemple de définition de propriété pour une propriété énumérée nommée risque d’incendie avec les valeurs possibles de faible, moyen et élevé.
  
```cpp
[Properties]
Property1 = Fire Hazard
[Enum1.HazardEnum]
IdxNmidPropset={E47F4480-8400-101B-934D-04021C007002]
IdxNmidString=FireHazardEnum
EnumCount = 3
Val.1.Display = Low
Val.1.Index = 1
Val.2.Display = Medium
Val.2.Index = 2
Val.3.Display = High
Val.3.Index = 3

```

 **[Enum1.** _chaîne_ sections **]** peuvent être utilisées par les applications pour deux raisons : pour accélérer le filtrage de propriétés à l’aide de l’index au lieu de la chaîne et pour trier selon un ordre différent de celui de l’ordre alphanumérique des valeurs de chaîne. Par exemple, le tri peut être effectué en fonction de l’ordre de faible moyen élevé au lieu d’ordre haut-bas moyenne. 
  

