---
title: Sum Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Renvoie la somme de toutes les valeurs de l’expression.
ms.openlocfilehash: fe412393b844d6c579653d0c646e74511b3d5f5e
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180704"
---
# <a name="sum-function-access-custom-web-app"></a>Sum Function (Access custom web app)

Renvoie la somme de toutes les valeurs de l’expression.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
## <a name="syntax"></a>Syntaxe

 **Sum** (*NumericExpression*)
  
La **fonction Sum** contient l’argument suivant.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Expression identifiant le champ qui contient les données numériques à ajouter ou expression qui effectue un calcul à l’aide des données de ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, d’une constante ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas une des autres fonctions d’agrégation SQL).  <br/> |

## <a name="remarks"></a>Remarques

La **fonction Sum** ignore les enregistrements qui contiennent des valeurs Null.
  
La **fonction Sum** ne peut être utilisée qu’avec des colonnes numériques.
  