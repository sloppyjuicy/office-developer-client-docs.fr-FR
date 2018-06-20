---
title: Références de feuille de calcul
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- références [excel 2007], feuille de calcul, références de feuille de calcul [Excel 2007], références de feuille de calcul externes [Excel 2007], feuille de calcul active [Excel 2007], [Excel 2007] de feuille de calcul active, feuille de calcul interne fait référence [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7089fb891c96be9182189e3a5f30057721cebbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782212"
---
# <a name="worksheet-references"></a>Références de feuille de calcul

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Une référence dans Microsoft Excel est un type de données qui fait référence à un bloc rectangulaire de cellules (qui peuvent être qu’une seule cellule), ou dans certains cas, un nombre de blocs disjoints de cellules. En interne, Excel utilise un type de référence pour les cellules de la feuille en cours, appelé une référence interne. N’importe quelle cellule qui n’est pas dans la feuille actuelle est décrit par un autre type de référence appelé référence externe. Voir la section suivante pour la définition d’active et en cours.
  
## <a name="active-vs-current"></a>Active et en cours

Dans Excel, le terme actif fait référence à ce que l’utilisateur visualise. Le classeur actif et la feuille de calcul sont celles que l’utilisateur est actuellement affiché ou, si Excel a perdu le focus vers une autre application, a été consultant Excel dernière lorsque le focus. La feuille active est toujours dans le classeur actif. Une ou plusieurs cellules sont sélectionnées dans la feuille active sont appelés des cellules actives. Si un objet incorporé a le focus, les cellules sélectionnées au dernier sont toujours actives. 
  
Le terme actuel fait référence à ce qui est le recalcul Excel. Le classeur actif et la feuille de calcul sont ceux qui sont actuellement en cours de recalcul. La feuille en cours est toujours dans le classeur actif. La cellule en cours de recalcul est appelée en tant que la cellule actuelle, ou, dans le cas d’une formule de tableau en cours de recalcul, les cellules en cours. 
  
Les points importants à retenir sont les suivantes :
  
- La cellule active de classeur/feuille de calcul / n’est pas généralement celle en cours, bien qu’il puisse être.
    
- Une fonction d’ajouter un Visual Basic pour le module d’Applications (VBA) ou une DLL ou XLL, est toujours appelée à partir de la cellule active dans la feuille en cours ou d’un d'entre eux dans le cas de recalcul multithread (MTR).
    
Nombreuses fonctions Excel qui fournissent des informations sur une cellule, une plage de cellules ou une feuille dans un classeur de faire la distinction entre le classeur actif, feuille, ou cellule et le classeur actif, feuille ou de la cellule. Cette différence est répercutée dans les types de données utilisés pour décrire les références aux blocs de cellules, comme décrit dans la section suivante.
  
## <a name="internal-and-external-worksheet-references"></a>Références de feuille de calcul internes et externes

La principale différence entre les références internes et externes est que le type de données de référence externe contient un identificateur pour la feuille de calcul et une description des cellules sont désignés. Une référence interne ne contient aucune référence à la feuille, il est implicite que la feuille est la feuille active. 
  
De nombreuses fonctions API C renvoient des références ou prennent des arguments de référence. Toutes les fonctions API C qui prend référence arguments accepte les références internes ou externes, à l’exception de la fonction **xlSheetNm** , qui requiert une référence externe. Certaines fonctions ne retournent que des références internes ou externes. Par exemple, la fonction de API C [xlfCaller](xlfcaller.md) renvoie une référence pour les cellules d’appel, par définition, dans la feuille active. La référence renvoyée est toujours une référence interne, bien que la fonction peut retourner les types non référence où la fonction n’est pas appelée à partir d’une cellule de feuille de calcul. La fonction de API C [xlSheetId](xlsheetid.md) renvoie toujours l’ID d’une feuille de calcul contenue dans un type de données de référence externe. 
  
Les autres différences majeures entre les types de références internes et externes est que le type de données de référence externe peut décrire plusieurs blocs disjoints de cellules sur la même feuille. Références internes peuvent décrire uniquement un seul bloc dans la feuille active. Références disjoints peuvent être passés à une fonction qui prend un argument de plage.
  
## <a name="see-also"></a>Voir aussi



[Concepts de programmation Excel](excel-programming-concepts.md)
  
[�valuer les noms et les autres Expressions de formule de feuille de calcul](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Feuille de calcul Excel et d’évaluation d’Expression](excel-worksheet-and-expression-evaluation.md)

