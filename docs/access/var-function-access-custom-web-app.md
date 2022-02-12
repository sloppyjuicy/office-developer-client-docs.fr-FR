---
title: Var Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Renvoie la variation statistique d’un échantillon de population représenté sous la mesure d’un ensemble de valeurs contenues dans un champ spécifié dans une requête.
ms.openlocfilehash: 45946a493bdd3742a29a3a8a53a51ff7274382f7
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773725"
---
# <a name="var-function-access-custom-web-app"></a>Var Function (Access custom web app)

Renvoie la variation statistique d’un échantillon de population représenté sous la mesure d’un ensemble de valeurs contenues dans un champ spécifié dans une requête.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="syntax"></a>Syntaxe

 **Var** (*NumericExpression*)
  
La **fonction Var** contient l’argument suivant.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Expression de texte identifiant le champ qui contient les données numériques à évaluer ou expression qui effectue un calcul à l’aide des données de ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, d’une constante ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas une des autres fonctions d’agrégation SQL). |

## <a name="remarks"></a>Remarques

 **Var** ne peut être utilisé qu’avec des colonnes numériques. Les valeurs Null sont ignorées. 