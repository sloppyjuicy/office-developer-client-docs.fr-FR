---
title: Section Fichier de configuration de formulaire [Propriétés]
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
# <a name="form-configuration-file-properties-section"></a>Section Fichier de configuration de formulaire [Propriétés]

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Propriétés]** répertorie l’ensemble complet des propriétés que le formulaire utilise et publie ; autrement dit, les propriétés qu’elle crée dans ses messages personnalisés que les applications clientes MAPI peuvent utiliser lors de l’affichage des colonnes, du filtrage des tables des matières, de la configuration de dossiers de résultats de recherche, etc. Chaque entrée de cette liste de propriétés fait référence à une **autre [Propriété.** _section_ **de chaîne ]** comme illustré ci-après. 
  
 **[Propriétés]**
  
 **Propriété.** _string_  =   _string_
  
Format d’un [ **Propriété.** _string_] est la suivante : 
  
 **[Propriété.** _string_ **]**
  
 **Type**  =   _integer_
  
 **NmidPropset**  =   _guid_
  
 **NmidString**  =   _string_
  
 **NmidInteger**  =   _integer_
  
 **DisplayName**  =   _string_
  
 **Indicateurs**  =   _integer_
  
 **SpecialType** = 0|1 
  
 **Enum1**  =   _string_
  
Chaque **[Propriété.** _section_ **]** décrit une seule propriété. **L’entrée** Type spécifie le type de propriété MAPI, par exemple 3 (PT_I4), de la propriété. **L’entrée NmidPropset** est facultative . avec l’entrée **NmidString** ou **NmidInteger,** l’entrée **NmidPropset** donne le nom de la propriété. **NmidString** donne le nom de la propriété, tandis que **NmidInteger** donne l’identificateur de la propriété. **NmidString et** **NmidInteger** s’excluent mutuellement. 
  
S’il est définie, **NmidPropset** doit contenir le nom du jeu de propriétés ; En cas d’absence, **NmidPropset** est définie sur une valeur par défaut basée sur la règle suivante : si **NmidInteger** est présent et que sa valeur est inférieure à 0x8000, **NmidPropset** est définie sur PS_MAPI. Si la valeur de **NmidInteger** est définie sur un nombre inférieur à 0x8000 ou si elle est absente, **NmidPropset** est définie sur PS_PUBLIC_STRINGS. 
  
**L’entrée DisplayName** contient l’étiquette de la propriété. **L’entrée SpecialType,** si elle est présente et non zéro, indique que cette propriété est une propriété spéciale. Pour l’instant, le seul type de propriété spécial défini est **SpecialType** = 1, qui indique les propriétés d’une chaîne. Si **SpecialType** est définie sur 1, l’entrée **Enum1** fait référence à **[Enum1.** _string_ **]** section. 
  
Voici un exemple de section **[Propriétés]** et **de [Propriétés.** _string_ **]** section. 
  
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

**L’entrée Enum1** dans l’exemple de précédation fait référence à une **autre [Enum1.** _section_ **de chaîne ]** décrivant une éumération d’un type particulier. Une telle éumération associe la première propriété de **[Property.** _section_ **de chaîne ]** avec une propriété de l’ensemble, appelée index. Cette énumération contient également une liste des valeurs possibles que la paire d’index d’affichage peut supposer. Il n’est pas nécessaire de spécifier un type de propriété pour l’PT_I4 car, par définition, une entrée **Enum1** a toujours le type PT_I4. Format de **[Enum1.** _la_ section **string ]** est la suivante : 
  
 **[Enum1.** _string_ **]**
  
 **NmidPropset**  =   _guid_
  
 **NmidString**  =   _string_
  
 **NmidInteger**  =   _integer_
  
 **EnumCount**  =   _integer_
  
 **Val.** _integer_ **. Chaîne d’affichage**  =   
  
 **Val.** _integer_ **.**  =   _Integer d’index_
  
Voici un exemple de définition de propriété pour une propriété éumée nommée Fire Danger avec des valeurs possibles de Low, Medium et High.
  
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

 **[Enum1.**  les sections de chaîne **]** peuvent être utilisées par les applications à deux fins : pour accélérer le filtrage des propriétés à l’aide de l’index au lieu de la chaîne et pour trier dans un ordre différent de l’ordre alphanumérique des valeurs de chaîne. Par exemple, le tri peut être effectué en fonction de l’ordre faible-moyen-élevé au lieu de l’ordre Élevé-Moyen-Bas. 
  

