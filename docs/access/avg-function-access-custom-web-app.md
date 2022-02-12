---
title: Avg Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcule la moyenne arithmétique d’un ensemble de valeurs contenues dans un champ spécifié.
ms.openlocfilehash: cb1c3aaac89e426917ef0ea8c54525e17d3e52ed
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771016"
---
# <a name="avg-function-access-custom-web-app"></a>Avg Function (Access custom web app)

Calcule la moyenne arithmétique d’un ensemble de valeurs contenues dans un champ spécifié.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="syntax"></a>Syntaxe

 **Avg** (*NumericExpression*)
  
La **fonction Avg** contient l’argument suivant.
  
|**Argument**|**Description**|
|:-----|:-----|
|NumericExpression  <br/> |Expression chaîne identifiant le champ qui contient les données numériques à moyenner ou une expression qui effectue un calcul à l’aide des données de ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, d’une variable ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas une des autres fonctions d’agrégation SQL). |

## <a name="remarks"></a>Remarques

La moyenne calculée par **Avg** est la moyenne arithmétique (la somme des valeurs divisée par le nombre de valeurs). Vous pouvez utilisez **Avg**, par exemple, pour calculer des frais de port moyens.
  
La **fonction Avg** n’inclut aucune valeur **Null** dans le calcul.
