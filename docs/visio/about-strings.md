---
title: À propos des chaînes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Les formules peuvent contenir des chaînes. Pour mettre en forme une chaîne, dans une cellule de message, une valeur d’élément de données de forme ou un champ, par exemple, vous devez définir un modèle de format. Le résultat peut être formaté sous forme de paire nombre-unité, de chaîne, de date-heure, de durée ou d’unité monétaire. Par exemple, le format picture0 #/10 uuformats les paires nombre-unité de 2 AS10 9/10 centimètres.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345065"
---
# <a name="about-strings"></a>À propos des chaînes

Les formules peuvent contenir des chaînes. Pour mettre en forme une chaîne, dans une cellule de message, une valeur d’élément de données de forme ou un champ, par exemple, vous devez définir un modèle de format. Le résultat peut être formaté sous forme de paire nombre-unité, de chaîne, de date-heure, de durée ou d’unité monétaire. Par exemple, le modèle de format « 0 #/10 uu » affiche la paire nombre-unité 10,9cm sous la forme « 10 9/10 centimètres ».
  
Vous pouvez utiliser les images de format dans la cellule **format** de la section données de forme et en tant qu'argument de la fonction **format** ou **FORMATEX** . Lorsque vous insérez un champ de texte, les modèles s’affichent dans la liste des formats de la boîte de dialogue **Champ** (onglet **Insertion**). 
  
## <a name="using-functions-to-format-strings"></a>Utilisation de fonctions pour mettre en forme des chaînes

Dans toute formule qui est résolue en chaîne, y compris les formules de champ de texte personnalisé, vous pouvez utiliser la fonction **format** ou **FORMATEX** . La fonction FORMAT renvoie une chaîne mise en forme. La fonction **FORMATEX** convertit une entrée non typée en unités choisies pour le résultat mis en forme. 
  
## <a name="displaying-formatted-shape-data"></a>Affichage des données de forme mises en forme

Vous pouvez mettre en forme la valeur affichée d’un élément de données de forme en indiquant un modèle de format dans la cellule Format.
  
Par exemple, une forme de planning peut être associée à un élément de données de forme permettant de mesurer le coût d’un processus. Par défaut, un élément de données de forme est une chaîne. Pour mettre en forme la chaîne « 1200 », vous pouvez entrer « ### ###,00 € » dans la cellule Format pour afficher le symbole monétaire.
  
Microsoft Visio utilise les paramètres de l’onglet **Devise** dans la boîte de dialogue **Personnaliser le format** de l’élément **Région et langue** du Panneau de configuration pour déterminer le symbole monétaire et le séparateur des milliers à afficher. (Dans **le panneau de configuration**, cliquez sur **région et langue**, puis cliquez sur **paramètres supplémentaires**.)
  
Pour convertir une chaîne en valeur monétaire afin d’effectuer des calculs, utilisez la fonction CY.
  
## <a name="using-functions-to-manipulate-text-strings"></a>Utilisation de fonctions pour manipuler des chaînes de texte

Vous pouvez utiliser des fonctions pour manipuler des chaînes de texte, par exemple, pour rechercher ou remplacer certains caractères dans une chaîne de texte. Il est également possible d’obtenir des informations concernant la position d’un caractère dans une chaîne ou d’identifier les caractères de début et de fin d’une chaîne de texte. 
  

