---
title: Égal à (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compare l'égalité de deux expressions.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308224"
---
# <a name="equals-access-custom-web-app"></a>Égal à (application Web personnalisée Access)

Compare l'égalité de deux expressions.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

`= (Equals)`

*expression*  =  *expression* 
  
*expression*  représente toute expression valide. Si les expressions n'ont pas le même type de données, le type de données d'une expression doit être implicitement convertible vers le type de données de l'autre. La conversion varie en fonction des règles de priorité des types de données. 
  
## <a name="return-type"></a>Type renvoyé

**Booléen**
  
## <a name="remarks"></a>Remarques

Lorsque vous comparez deux expressions de type NULL, le résultat est TRUE.
  
La comparaison de NULL à une valeur non NULL aboutit toujours à FALSe.
  

