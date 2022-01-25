---
title: Références de feuille de calcul
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- references [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
ms.openlocfilehash: 07033f18054c279244fdbb8ed314396bcd40326b
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198729"
---
# <a name="worksheet-references"></a>Références de feuille de calcul

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Une référence dans Microsoft Excel est un type de données qui fait référence à un bloc rectangulaire de cellules (qui ne peut être qu’une seule cellule) ou, dans certains cas, à un certain nombre de blocs de cellules disjoints. En interne, Excel utilise un type de référence pour les cellules de la feuille actuelle, appelée référence interne. Toute cellule qui ne se trouve pas dans la feuille actuelle est décrite par un autre type de référence appelé référence externe. Consultez la section suivante pour obtenir la définition des valeurs active et actuelle.
  
## <a name="active-vs-current"></a>Actif ou actif

Dans Excel, le terme actif fait référence à ce que l’utilisateur affiche. Le workbook et la feuille de calcul actifs sont ceux que l’utilisateur recherche actuellement, ou, si Excel a perdu le focus sur une autre application, était à la recherche lorsque Excel a eu le focus pour la dernière fois. La feuille active se trouve toujours dans le livre de travail actif. Les cellules sélectionnées dans la feuille active sont appelées cellules actives. Si un objet incorporé a le focus, les dernières cellules sélectionnées sont toujours actives. 
  
Le terme actuel fait référence au Excel le recalcul. Le workbook et la feuille de calcul actuels sont ceux qui sont actuellement recalculés. La feuille actuelle se trouve toujours dans le manuel en cours. La cellule en cours de recalcul est appelée la cellule actuelle ou, dans le cas d’une formule de tableau en cours de recalcul, les cellules actuelles. 
  
Les points importants à retenir sont les suivants :
  
- Le workbook/worksheet/cell actif n’est généralement pas celui en cours, bien qu’il puisse l’être.
    
- Une fonction de add-in, que ce soit dans un module Visual Basic pour Applications (VBA), une DLL ou une XLL, est toujours appelée à partir de la cellule actuelle de la feuille actuelle, ou l’une d’elles dans le cas d’un recalcul multithread (MTR).
    
De nombreuses Excel qui fournissent des informations sur une cellule, une plage de cellules ou une feuille d’un manuel font la distinction entre le workbook actif, la feuille ou la cellule et le workbook, la feuille ou la cellule actif. Cette différence est reflétée dans les types de données utilisés pour décrire les références à des blocs de cellules, comme décrit dans la section suivante.
  
## <a name="internal-and-external-worksheet-references"></a>Références internes et externes aux feuilles de calcul

La principale différence entre les références internes et externes est que le type de données de référence externe contient un ID pour la feuille de calcul, ainsi qu’une description des cellules référencés. Une référence interne ne contient aucune référence à la feuille ; il est implicite que la feuille soit la feuille actuelle. 
  
De nombreuses fonctions d’API C retournent des références ou prennent des arguments de référence. Toute fonction API C qui accepte des arguments de référence accepte des références internes ou externes, à l’exception de la fonction **xlSheetNm,** qui nécessite une référence externe. Certaines fonctions retournent uniquement des références internes ou externes. Par exemple, la fonction API C [xlfCaller](xlfcaller.md) renvoie une référence aux cellules d’appel, par définition, dans la feuille actuelle. La référence renvoyée est toujours une référence interne, bien que la fonction puisse renvoyer des types non référencés lorsque la fonction n’est pas appelée à partir d’une cellule de feuille de calcul. La fonction API C [xlSheetId](xlsheetid.md) renvoie toujours l’ID d’une feuille de calcul contenue dans un type de données de référence externe. 
  
L’autre différence clé entre les types de référence interne et externe est que le type de données de référence externe peut décrire plusieurs blocs de cellules disjoints sur la même feuille. Les références internes ne peuvent décrire qu’un seul bloc de la feuille actuelle. Les références disjointes peuvent être transmises à n’importe quelle fonction qui prend un argument de plage.
  
## <a name="see-also"></a>Voir aussi



[Concepts de programmation Excel](excel-programming-concepts.md)
  
[Évaluer les noms et les autres Expressions de formule de feuille de calcul](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Feuille de calcul et évaluation des expressions Excel](excel-worksheet-and-expression-evaluation.md)

