---
title: Count function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Renvoie le nombre d’enregistrements dans une requête ou une table.
ms.openlocfilehash: 3431c90b0c128ace57fd251196e1d64956183f9e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777851"
---
# <a name="count-function-access-custom-web-app"></a>Count function (Access custom web app)

Renvoie le nombre d’enregistrements dans une requête ou une table.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="syntax"></a>Syntaxe

**Count** (*Expression*)
  
La **fonction Count** contient l’argument suivant.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Expression*  <br/> |Expression chaîne identifiant le champ qui contient les données à compter ou expression qui effectue un calcul à l’aide des données du champ. Les opérandes dans *Expression* peuvent inclure le nom d’un champ de table ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas d’SQL fonctions d’agrégation). Vous pouvez compter tous les types de données, y compris du texte. |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser Count pour compter le nombres d'enregistrements dans une requête sous-jacente. Par exemple, vous pouvez utiliser Count pour compter le nombre de commandes expédiées vers un pays ou une région particulier.
  
**Count** (\*) renvoie le nombre d’éléments dans un groupe. Cela inclut les valeurs NULL et les doublons.
