---
title: Fonction CharIndex (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Recherche une autre expression de texte dans une expression de texte et renvoie sa position de départ si elle est trouvée.
ms.openlocfilehash: f0c320c7314e109588eabd4d7d8429546b51b0a9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370546"
---
# <a name="charindex-function-access-custom-web-app"></a>Fonction CharIndex (application web personnalisée Access)

Recherche une autre expression de texte dans une expression de texte et renvoie sa position de départ si elle est trouvée.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="syntax"></a>Syntaxe

**CharIndex** (*TextExpression*, *WithinText*, [*Start*])
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Oui  <br/> |Expression de texte qui contient le texte à trouver. |
| *WithinText*  <br/> |Oui  <br/> |Expression de texte à rechercher. |
| *Start*  <br/> |Non  <br/> |Nombre intégral qui spécifie l’emplacement dans *WithinText* pour commencer la recherche. Si *l’indication* Start n’est pas spécifiée, est un nombre négatif ou est 0, la recherche commence au début de *WithinText*. |

## <a name="remarks"></a>Remarques

Si *TextExpression ou* *WithinText a la* valeur NULL, *CharIndex renvoie* la valeur NULL.
  
Si *TextExpression n’est* pas trouvé *dans WithinText*, *CharIndex renvoie* 0.
  
La position de départ renvoyée est basée sur 1, et non sur 0.
  