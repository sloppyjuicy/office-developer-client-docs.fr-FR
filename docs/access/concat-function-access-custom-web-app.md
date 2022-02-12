---
title: Fonction Concat (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Renvoie une chaîne qui est le résultat de la combinaison de deux ou plusieurs valeurs de chaîne.
ms.openlocfilehash: fa99f6d09e0d80bb091343b27fc60028297c3ef6
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770981"
---
# <a name="concat-function-access-custom-web-app"></a>Fonction Concat (application web personnalisée Access)

Renvoie une chaîne qui est le résultat de la combinaison de deux ou plusieurs valeurs de chaîne.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**Concat** (*valeur1*, *valeur2*, ... [*ValueN*]) 
  
La **fonction Concat** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
|Valeur  <br/> |Valeur de chaîne à concaténer aux autres valeurs. |
   
## <a name="remarks"></a>Remarques

**Concat** prend un nombre variable d’arguments de chaîne et les concatène en une seule chaîne. Un minimum de deux arguments de chaîne est requis ; Dans le cas contraire, une erreur est produite. 
  
Tous les arguments sont implicitement convertis en types de données de chaîne, puis concatés.
  
## <a name="example"></a>Exemple

L’expression suivante peut être utilisée pour afficher le nom complet d’une personne où la table contient les champs FirstName, MiddleInitial et LastName. Si le champ MiddleInitial est vide, seuls les champs FirstName et LastName sont combinés pour afficher le nom complet.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


