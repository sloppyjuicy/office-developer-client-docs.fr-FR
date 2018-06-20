---
title: Fonction CharIndex (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Recherche une expression de texte pour une autre expression de texte et renvoie son démarrage position si trouvé.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781837"
---
# <a name="charindex-function-access-custom-web-app"></a>Fonction CharIndex (accès personnalisé web app)

Recherche une expression de texte pour une autre expression de texte et renvoie son démarrage position si trouvé.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**CharIndex** (*TextExpression*, *WithinText*, [*Démarrer*]) 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Oui  <br/> |Une expression de texte qui contient le texte à rechercher.  <br/> |
| *WithinText*  <br/> |Oui  <br/> |L’expression de texte à rechercher.  <br/> |
| *Début*  <br/> |Non  <br/> |Entier qui spécifie l’emplacement dans *WithinText* pour commencer la recherche. Si *Démarrer* n’est pas spécifié, est un nombre négatif ou est égale à 0, la recherche commence au début de *WithinText* .  <br/> |
   
## <a name="remarks"></a>Remarques

Si *TextExpression* ou *WithinText* est NULL, *CharIndex* renvoie la valeur NULL. 
  
Si *TextExpression* est introuvable dans *WithinText*, *CharIndex* renvoie la valeur 0. 
  
La position de départ retournée est de base 1, et non de base 0.
  

