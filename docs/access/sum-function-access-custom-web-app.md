---
title: Sum Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Renvoie la somme de toutes les valeurs de l’expression.
ms.openlocfilehash: 2e6b75d256776e9552939e124410d258be1c0d74
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605700"
---
# <a name="sum-function-access-custom-web-app"></a>Sum Function (Access custom web app)

Renvoie la somme de toutes les valeurs de l’expression.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Sum** (*NumericExpression*) 
  
La **fonction Sum** contient l’argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Expression identifiant le champ qui contient les données numériques à ajouter ou expression qui effectue un calcul à l’aide des données de ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, d’une constante ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas l’une des autres fonctions d’agrégation SQL).  <br/> |
   
## <a name="remarks"></a>Remarques

La **fonction Sum** ignore les enregistrements qui contiennent des valeurs Null. 
  
La **fonction Sum** ne peut être utilisée qu’avec des colonnes numériques. 
  

