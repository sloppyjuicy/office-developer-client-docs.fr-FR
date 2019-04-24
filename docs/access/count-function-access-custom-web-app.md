---
title: Fonction count (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Renvoie le nombre d'enregistrements dans une requête ou une table.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282235"
---
# <a name="count-function-access-custom-web-app"></a>Fonction count (application Web personnalisée Access)

Renvoie le nombre d'enregistrements dans une requête ou une table.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**Nombre** (*Expression*) 
  
La fonction **Count** contient l'argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Expression*  <br/> |Expression de chaîne identifiant le champ qui contient les données que vous souhaitez compter ou une expression qui effectue un calcul à l'aide des données du champ. Les opérandes dans *expression* peuvent inclure le nom d'un champ de table ou une fonction (qui peut être intrinsèque ou définie par l'utilisateur, mais pas avec d'autres fonctions d'agrégation SQL). Vous pouvez compter tous les types de données, y compris du texte.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser Count pour compter le nombres d'enregistrements dans une requête sous-jacente. Par exemple, vous pouvez utiliser Count pour compter le nombre de commandes expédiées vers un pays ou une région spécifique.
  
**Nombre** (\*) renvoie le nombre d'éléments dans un groupe. Cela inclut les valeurs NULL et les doublons. 
  

