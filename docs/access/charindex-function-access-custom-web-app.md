---
title: Fonction CharIndex (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Recherche une expression de texte pour une autre expression de texte et renvoie sa position de départ si elle est trouvée.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282606"
---
# <a name="charindex-function-access-custom-web-app"></a>Fonction CharIndex (application Web personnalisée Access)

Recherche une expression de texte pour une autre expression de texte et renvoie sa position de départ si elle est trouvée.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**CharIndex** (*TextExpression*, *WithinText*, [*Start*]) 
  
|**Nom de l'argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Oui  <br/> |Expression de texte qui contient le texte à rechercher.  <br/> |
| *WithinText*  <br/> |Oui  <br/> |Expression de texte à rechercher.  <br/> |
| *Start*  <br/> |Non  <br/> |Entier qui spécifie l'emplacement dans *WithinText* pour commencer la recherche. Si *Start* n'est pas spécifié, est un nombre négatif ou est égal à 0, la recherche commence au début de *WithinText* .  <br/> |
   
## <a name="remarks"></a>Remarques

Si *TextExpression* ou *WithinText* est NULL, *charIndex* renvoie null. 
  
Si *TextExpression* est introuvable dans *WithinText*, *charIndex* renvoie 0. 
  
La position de départ renvoyée est de base 1, et non de base 0.
  

