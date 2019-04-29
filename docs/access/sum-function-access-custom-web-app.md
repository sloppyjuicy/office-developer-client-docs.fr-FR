---
title: Fonction Sum (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Renvoie la somme de toutes les valeurs de l'expression.
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427100"
---
# <a name="sum-function-access-custom-web-app"></a>Fonction Sum (application Web personnalisée Access)

Renvoie la somme de toutes les valeurs de l'expression.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Somme** (*NumericExpression*) 
  
La fonction **Sum** contient l'argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Expression identifiant le champ qui contient les données numériques que vous souhaitez ajouter ou une expression qui effectue un calcul à l'aide des données de ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d'un champ de table, une constante ou une fonction (qui peut être soit intrinsèque, soit définie par l'utilisateur, mais pas une des autres fonctions d'agrégation SQL).  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction **Sum** ignore les enregistrements qui contiennent des valeurs NULL. 
  
La fonction **Sum** ne peut être utilisée qu'avec des colonnes numériques. 
  

