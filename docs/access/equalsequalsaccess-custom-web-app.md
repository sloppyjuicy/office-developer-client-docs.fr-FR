---
title: Est égale à (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compare l’égalité de deux expressions.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781839"
---
# <a name="equals-access-custom-web-app"></a>Est égale à (accès personnalisé web app)

Compare l’égalité de deux expressions.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

`= (Equals)`

*expression*  =  *expression* 
  
*expression*  Peut être toute expression valide. Si les expressions ne sont pas du même type de données, le type de données pour une expression doit être implicitement convertible au type de données de l’autre. La conversion dépend des règles de priorité des types de données. 
  
## <a name="return-type"></a>Type renvoyé

**Booléen**
  
## <a name="remarks"></a>Notes

Lorsque vous comparez deux expressions NULL, le résultat est TRUE.
  
Comparaison toujours NULL pour une valeur non NULL donne FALSE.
  

