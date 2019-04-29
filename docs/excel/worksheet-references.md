---
title: Références de feuille de calcul
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- références [Excel 2007], feuille de calcul, références de feuille de calcul [Excel 2007], références de feuille de calcul externes [Excel 2007], feuille de calcul active [Excel 2007], feuille de calcul active [Excel 2007], références de feuille de calcul interne [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2944f73a3144837a4be8aff7c7fed9a8d2158203
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416460"
---
# <a name="worksheet-references"></a>Références de feuille de calcul

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Une référence dans Microsoft Excel est un type de données qui fait référence à un bloc de cellules rectangulaire (qui peut être une seule cellule) ou dans certains cas, un certain nombre de blocs de cellules disjoints. En interne, Excel utilise un type référence pour les cellules de la feuille actuelle, appelée référence interne. Toute cellule qui ne figure pas dans la feuille actuelle est décrite par un autre type de référence appelé référence externe. Consultez la section suivante pour obtenir la définition des actifs et des actuels.
  
## <a name="active-vs-current"></a>Actif et actuel

Dans Excel, le terme actif fait référence à ce que l'utilisateur visualise. Le classeur et la feuille de calcul actifs sont ceux que l'utilisateur consulte actuellement, ou si Excel a perdu le focus vers une autre application, il consultait la dernière fois qu'Excel avait le focus. La feuille active se trouve toujours dans le classeur actif. La ou les cellules sélectionnées dans la feuille active sont connues sous le nom de cellules actives. Si un objet incorporé a le focus, les cellules de dernière sélection sont toujours actives. 
  
Le terme «actuel» fait référence à ce qu'Excel recalcule. Le classeur actif et la feuille de calcul sont ceux qui sont actuellement recalculés. La feuille active se trouve toujours dans le classeur actif. La cellule en cours de Recalculation est appelée cellule active ou, dans le cas d'une formule matricielle recalculée, les cellules actives. 
  
Les points importants à garder à l'esprit sont les suivants:
  
- Le classeur/feuille de calcul/cellule actif n'est généralement pas l'actuel, bien qu'il puisse l'être.
    
- Une fonction de complément, qu'elle se trouve dans un module Visual Basic pour applications (VBA) ou une DLL ou XLL, est toujours appelée à partir de la cellule active de la feuille active ou de l'une d'elles dans le cas d'un recalcul multithread (du recalcul MULTITHREAD).
    
De nombreuses fonctions Excel qui fournissent des informations sur une cellule, une plage de cellules ou une feuille dans un classeur font la distinction entre le classeur, la feuille ou la cellule actif et le classeur, feuille ou cellule actif. Cette différence est reflétée dans les types de données utilisés pour décrire les références à des blocs de cellules, comme décrit dans la section suivante.
  
## <a name="internal-and-external-worksheet-references"></a>Références de feuille de calcul interne et externe

La principale différence entre les références internes et externes est que le type de données de référence externe contient un ID pour la feuille de calcul, ainsi qu'une description des cellules auxquelles il est fait référence. Une référence interne ne contient aucune référence à la feuille: il s'agit implicite de la feuille active. 
  
De nombreuses fonctions de l'API C renvoient des références ou prennent des arguments de référence. Toute fonction d'API C qui prend des arguments de référence accepte des références internes ou externes, à l'exception de la fonction **xlSheetNm** , qui requiert une référence externe. Certaines fonctions renvoient des références internes ou externes. Par exemple, la fonction API C [xlfCaller](xlfcaller.md) renvoie une référence aux cellules d'appel, par définition, sur la feuille actuelle. La référence renvoyée est toujours une référence interne, bien que la fonction puisse renvoyer des types non référencés où la fonction n'est pas appelée à partir d'une cellule de feuille de calcul. La fonction API C [xlSheetId](xlsheetid.md) renvoie toujours l'ID d'une feuille de calcul contenue dans un type de données de référence externe. 
  
L'autre différence clé entre les types de référence interne et externe est que le type de données de référence externe peut décrire plusieurs blocs de cellules disjoints dans la même feuille. Les références internes ne peuvent décrire qu'un seul bloc sur la feuille actuelle. Les références disjointes peuvent être transmises à toute fonction qui prend un argument de plage.
  
## <a name="see-also"></a>Voir aussi



[Concepts de programmation Excel](excel-programming-concepts.md)
  
[Évaluer les noms et les autres Expressions de formule de feuille de calcul](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Feuille de calcul et évaluation des expressions Excel](excel-worksheet-and-expression-evaluation.md)

