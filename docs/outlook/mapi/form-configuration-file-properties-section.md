---
title: Section [propriétés] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421290"
---
# <a name="form-configuration-file-properties-section"></a>Section [propriétés] du fichier de configuration de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Properties]** répertorie l'ensemble complet des propriétés que le formulaire utilise et publie; autrement dit, les propriétés qu'il crée dans ses messages personnalisés que les applications clientes MAPI peuvent utiliser lors de l'affichage des colonnes, du filtrage des tables de contenu, de la configuration des dossiers de résultats de recherche, etc. Chaque entrée de cette liste de propriétés fait référence à une **propriété suivante.** _String (chaîne_ ) **]** , comme illustré ci-dessous. 
  
 **Propriétés**
  
 **Inspecteur.** __ =  _chaîne_ de chaîne
  
Format d'une propriété [ **.** _chaîne_] la section est la suivante: 
  
 **Inspecteur.** _String (chaîne_ ) **]**
  
 **Type** =  _entier_
  
 **** =  _GUID_ NmidPropset
  
 **** =  _Chaîne_ NmidString
  
 **** =  _Entier_ NmidInteger
  
 **** =  _Chaîne_ DisplayName
  
 **Indicateurs** =  de_nombre entier_
  
 **SpecialType** = 0 | 1 
  
 **** =  _Chaîne_ Enum1
  
Each **[Property.** _String (chaîne_ ) **]** décrit une propriété unique. L'entrée **type** spécifie le type de propriété MAPI, par exemple 3 (PT_I4), de la propriété. L'entrée **NmidPropset** est facultative; avec l'entrée **NmidString** ou l'entrée **NmidInteger** , l'entrée **NmidPropset** indique le nom de la propriété. **NmidString** indique le nom de la propriété, tandis que **NmidInteger** renvoie l'identificateur de la propriété. **NmidString** et **NmidInteger** s'excluent mutuellement. 
  
S'il est défini, **NmidPropset** doit contenir le nom du jeu de propriétés; Si elle est absente, **NmidPropset** est défini sur une valeur par défaut basée sur la règle suivante: si **NmidInteger** est présent et que sa valeur est inférieure à 0x8000, **NmidPropset** est défini sur PS_MAPI. Si la valeur de **NmidInteger** est définie sur un entier supérieur à 0x8000 ou si elle est absente, **NmidPropset** est défini sur PS_PUBLIC_STRINGS. 
  
L'entrée **DisplayName** contient l'étiquette de la propriété. L'entrée **SpecialType** , si elle est présente et différente de zéro, indique que cette propriété est une propriété spéciale. Actuellement, le seul type de propriété spéciale défini est **SpecialType** = 1, qui indique les propriétés énumérées de la chaîne. Si **SpecialType** est défini sur 1, l'entrée **Enum1** fait référence à **[Enum1.** _String (chaîne_ ) **]** . 
  
Voici un exemple de section **[Properties]** et a **[Properties].** _String (chaîne_ ) **]** . 
  
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

L'entrée **Enum1** dans l'exemple précédent fait référence à une nouvelle **[Enum1.** _String (chaîne_ ) **]** section décrivant une énumération d'un type particulier. Une telle énumération associe la première propriété de la **propriété [Property.** _String (chaîne_ ) **]** avec une propriété de type Integer, appelée index. Une telle énumération contient également une liste des valeurs possibles que la paire d'index d'affichage peut supposer. La spécification d'un type de propriété pour l'énumération n'est pas nécessaire, car par définition une entrée **Enum1** a toujours le type PT_I4. Format du **[Enum1.** _String (chaîne_ ) **]** est la suivante: 
  
 **[Enum1.** _String (chaîne_ ) **]**
  
 **** =  _GUID_ NmidPropset
  
 **** =  _Chaîne_ NmidString
  
 **** =  _Entier_ NmidInteger
  
 **** =  _Entier_ EnumCount
  
 **Val.** _nombre entier_ **. ** =  _Chaîne_ d'affichage
  
 **Val.** _nombre entier_ **. ** =  _Entier_ de l'index
  
Vous trouverez ci-dessous un exemple de définition de propriété pour une propriété énumérée nommée risque d'incendie, avec les valeurs possibles: faible, moyen et élevé.
  
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

 **[Enum1.** _String (chaîne_ ) **]** les sections peuvent être utilisées par les applications à deux fins: accélérer le filtrage des propriétés à l'aide de l'index au lieu de la chaîne et trier selon un ordre différent de l'ordre alphanumérique des valeurs de la chaîne. Par exemple, le tri peut être réalisé en fonction de la commande à faible-moyen-haut au lieu de la commande haut-moyen-bas. 
  

