---
title: À propos des fonctions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251825
ms.localizationpriority: medium
ms.assetid: 871b8601-8117-bc51-17b9-6002234b4bfb
description: "Une fonction effectue une tâche unique et bien précise. La plupart des fonctions acceptent plusieurs arguments comme entrées. Le type et le nombre d'arguments dépendent des fonctions, mais toutes utilisent la même syntaxe générale :"
ms.openlocfilehash: 3642d4ac3cb692d542db14bcc20eef06f05985c7
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63508221"
---
# <a name="about-functions"></a>À propos des fonctions

Une fonction effectue une tâche unique et bien précise. La plupart des fonctions acceptent plusieurs arguments comme entrées. Le type et le nombre d'arguments dépendent des fonctions, mais toutes utilisent la même syntaxe générale :
  
 **FUNCTION(** _argument1_, _argument2_, ... _argumentN_ [, _argumentAargument_  | **])**
  
|**Élément syntaxique**|**Description**|
|:-----|:-----|
| ( )  <br/> | Si une fonction n'accepte pas d'arguments, elle doit être suivie d'une paire de parenthèses vide (). |
| ,  <br/> | Les arguments sont séparés par une virgule. |
| ... | Utilisé pour la notation uniquement ; ne pas inclure dans une fonction. |
| [ ]  <br/> | Argument facultatif. Utilisé pour la notation uniquement ; ne pas inclure dans une fonction. |
| \|  <br/> | Un choix ; vous pouvez inclure  _argumentA_ ou  _argument_. Utilisé pour la notation uniquement ; ne pas inclure dans une fonction. |

De nombreuses fonctions utilisables dans les formules ressemblent à celles que vous avez l'habitude de rencontrer dans les tableurs : fonctions mathématiques, comme SUM ou SQRT ; trigonométriques, comme SIN ou COS, ou logiques, comme IF ou NOT. Beaucoup d'autres fonctions sont toutefois propres à Microsoft Office Visio, par exemple GUARD, GRAVITY et RUNADDON.
  
Pour plus d'informations sur des fonctions spécifiques, reportez-vous à l'aide Référence ShapeSheet.
  
> [!NOTE]
> Certaines fonctions apparaissent dans les formules générées par Visio, mais ne sont pas affichées dans la  boîte de dialogue Modifier la formule ou décrites dans cette référence, car elles sont réservées à un usage interne et ne doivent pas être utilisées dans d’autres formules. Voici quelques exemples : ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1 et _SHAPEMIN.
  