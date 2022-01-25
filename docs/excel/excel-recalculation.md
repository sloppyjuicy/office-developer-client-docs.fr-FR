---
title: Recalcul Excel
manager: kelbow
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- calcul forcé [Excel 2007], recalcul sélectif [Excel 2007], fonctions [Excel 2007], volatile,modes de calcul, cellules recalculées [Excel 2007], dépendance [Excel 2007], calcul feuille de calcul spécifiée [Excel 2007],recalcul [Excel 2007], reconstruction arborescence classeur [Excel 2007], calcul de plage [Excel 2007], recalcul d'Excel, fonctions volatiles [Excel 2007], fonctions [Excel 2007], non-volatiles, calcul de feuille de calcul active [Excel 2007], cellules sales [Excel 2007], fonctions non-volatiles [Excel 2007], recalcul forcé [Excel 2007].
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
ms.localizationpriority: high
ms.openlocfilehash: 19823be3a1685d8f64c116db2f36f3abfd71f952
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198988"
---
# <a name="excel-recalculation"></a>Recalcul Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
L’utilisateur peut déclencher le recalcul dans Microsoft Excel de plusieurs façons :
  
- en saisissant de nouvelles données (si Excel est en mode de recalcul automatique, décrit plus loin dans cette rubrique) ;
- en demandant explicitement à Excel de recalculer l’intégralité ou la partie d’un classeur ;
- en supprimant ou insérant une ligne ou colonne ;
- en enregistrant un classeur alors que l’option **Recalcul avant l’enregistrement** est définie ;
- en exécutant certaines actions de filtrage automatique ;
- en cliquant deux fois sur un séparateur de ligne ou de colonne (en mode de calcul automatique) ;
- en ajoutant, modifiant ou supprimant un nom défini ;
- en renommant une feuille de calcul ;
- en modifiant la position d’une feuille de calcul liée à d’autres feuilles de calcul ;
- en masquant ou affichant des lignes, mais pas des colonnes.

> [!NOTE]
> Cette rubrique ne fait pas la différence entre l’utilisateur appuyant sur une touche ou cliquant sur la souris, et les tâches effectuées par une commande ou une macro. L’utilisateur exécute la commande, ou fait quelque chose pour déclencher l’exécution de la commande, de façon à ce que ce soit considéré comme une action de l’utilisateur. C’est pourquoi les termes « l’utilisateur » signifient également « l’utilisateur, ou une commande ou processus exécuté par l’utilisateur ».
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>Dépendance, cellules incorrectes et cellules recalculées

Le calcul des feuilles de calcul dans Excel peut être considéré comme un processus à trois étapes :
  
1. Construction d’une arborescence des dépendances
2. Construction d’une chaîne de calcul
3. Recalcul de cellules

L’arborescence des dépendances indique à Excel les cellules dépendant d’autres cellules, ou de façon équivalente, les cellules qui sont les antécédents d’autres cellules. À partir de cette arborescence, Excel crée une chaîne de calcul. Celle-ci répertorie toutes les cellules qui contiennent des formules dans l’ordre dans lequel elles doivent être calculées. Pendant le recalcul, Excel modifie cette chaîne s’il rencontre une formule qui dépend d’une cellule qui n’a pas encore été calculée. Dans ce cas, la cellule est calculée, et les cellules qui en dépendent sont déplacées vers le bas de la chaîne. Pour cette raison, les durées de calcul peuvent souvent être réduites dans une feuille de calcul ayant juste été ouverte lors des premiers cycles de calcul.
  
Lorsqu’une modification structurelle est apportée à un classeur, par exemple lorsqu’une nouvelle formule est saisie, Excel reconstruit l’arborescence des dépendances et la chaîne de calcul. Lors de la saisie de nouvelles données ou formules, Excel marque toutes les cellules qui dépendent de ces nouvelles données comme nécessitant un recalcul. Les cellules marquées de cette manière sont appelées *incorrectes*. Toutes les cellules directement et indirectement dépendantes sont marquées comme incorrectes. De ce fait, si B1 dépend d’A1 et que C1 dépend de B1, lorsque A1 est modifiée, B1 et C1 sont marquées comme incorrectes.
  
Si une cellule dépend directement ou indirectement d’elle-même, Excel détecte la référence circulaire et avertit l’utilisateur. Il s’agit généralement d’une condition d’erreur que l’utilisateur doit résoudre, et Excel fournit des outils de graphique et de navigation très utiles pour aider l’utilisateur à trouver la source de la dépendance circulaire. Dans certains cas, vous voudrez délibérément que cette condition existe. Par exemple, vous souhaiterez peut-être exécuter un calcul itératif où le point de départ pour l’itération suivante est le résultat de l’itération précédente. Excel prend en charge le contrôle des calculs itératifs via la boîte de dialogue des options de calcul.
  
Une fois que certaines cellules sont marquées comme incorrectes, lorsqu’un recalcul est effectué, Excel réévalue le contenu de chaque cellule incorrecte dans l’ordre déterminé par la chaîne de calcul. Dans l’exemple donné précédemment, cela signifie que B1 est calculée en premier lieu, suivie par C1. Ce calcul a lieu immédiatement après qu’Excel a terminé de marquer les cellules comme incorrectes si le mode de recalcul est automatique. Sinon, il se produit plus tard.
  
À partir de Microsoft Excel 2002, l’objet **Range** dans Microsoft Visual Basic pour Applications (VBA) prend en charge une méthode, **Range.Dirty**, qui indique les cellules nécessitant un calcul. Lorsqu’elle est utilisée conjointement à la méthode **Range.Calculate** (voir la section suivante), elle permet le recalcul forcé de cellules dans une plage donnée. Cela est utile lorsque vous effectuez un calcul limité au cours d’une macro, où le mode de calcul est défini sur manuel, afin d’éviter la surcharge de calcul de cellules non liées à la fonction de macro. Les méthodes de calcul de plage ne sont pas disponibles via l’API C.
  
Dans Excel 2002 et versions antérieures, Excel a construit une chaîne de calcul pour chaque feuille de calcul dans chaque classeur ouvert. Cela a généré une certaine complexité dans la gestion des liens entre les feuilles de calcul, et a demandé de l’attention pour garantir un recalcul efficace. En particulier, dans Excel 2000, vous devez réduire les dépendances entre les classeurs et nommer les feuilles de calcul par ordre alphabétique, afin que les feuilles dépendant d’autres feuilles apparaissent après les feuilles dont elles dépendent.
  
Dans Excel 2007, la logique a été améliorée pour permettre le recalcul sur plusieurs threads afin que les sections de la chaîne de calcul ne soient pas interdépendantes et puissent être calculées en même temps. Vous pouvez configurer Excel pour utiliser plusieurs threads sur un ordinateur monoprocesseur ou un thread unique sur un ordinateur multiprocesseur ou multicœur.
  
## <a name="asynchronous-user-defined-functions-udfs"></a>Fonctions définies par l’utilisateur (UDF) asynchrones

Lorsqu’un calcul rencontre une UDF asynchrone, il enregistre l’état de la formule en cours, démarre l’UDF et continue l’évaluation des autres cellules. Lorsque le calcul termine l’évaluation des cellules, Excel attend que les fonctions asynchrones se terminent s’il en existe encore en cours d’exécution. Lorsque les fonctions asynchrones génèrent des résultats, Excel termine la formule et exécute une nouvelle phase de calcul pour recalculer les cellules qui utilisent la cellule référencée à la fonction asynchrone.
  
## <a name="volatile-and-non-volatile-functions"></a>Fonctions volatiles et non volatiles

Excel prend en charge le concept d’une fonction volatile, c’est-à-dire d’une fonction dont la valeur ne peut pas rester la même d’un moment à l’autre, même si aucun de ses arguments (si elle en a) n’a été modifié. Excel réévalue les cellules contenant des fonctions volatiles, ainsi que toutes les cellules dépendantes, chaque fois qu’il réalise un recalcul. C’est pourquoi un nombre trop élevé de fonctions volatiles peut ralentir le recalcul. Utilisez-les avec parcimonie.
  
Les fonctions Excel suivantes sont volatiles :
  
- **NOW**
- **TODAY**
- **RANDBETWEEN**
- **OFFSET**
- **INDIRECT**
- **INFO** (en fonction de ses arguments)
- **CELL** (en fonction de ses arguments)
- **SUMIF** (en fonction de ses arguments)

Les VBA et l’API C prennent en charge des méthodes pour indiquer à Excel qu’une fonction définie par l’utilisateur (UDF) doit être traitée comme une fonction volatile. À l’aide de VBA, l’UDF est déclarée comme volatile de la manière suivante.
  
```vba
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile MakeMeVolatile
   MyUDF = Now
End Function

```

Par défaut, Excel suppose que les UDF VBA ne sont pas volatiles. Excel apprend qu’une UDF est volatile lorsqu’il l’appelle pour la première fois. Une UDF volatile peut être modifiée en non volatile comme dans l’exemple suivant.
  
À l’aide de l’API C, vous pouvez enregistrer une fonction XLL comme étant volatile avant son premier appel. Elle permet également d’activer et de désactiver le statut volatile d’une fonction de feuille de calcul.
  
Par défaut, Excel gère les UDF XLL qui acceptent des arguments de plage et qui sont déclarées comme feuilles macro, équivalent de volatiles. Vous pouvez désactiver cet état par défaut à l’aide de la fonction **xlfVolatile** lorsque l’UDF est appelée pour la première fois.
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>Modes de calcul, commandes, recalcul sélectif et tables de données

Excel propose trois modes de calcul :
  
- Automatic
- Automatique sauf dans les tables
- Manual

Lorsque le calcul est défini sur Automatique, le recalcul se produit après chaque entrée de données, et après certains événements tels que les exemples fournis dans la section précédente. Pour les classeurs très volumineux, le temps de recalcul peut être si long que les utilisateurs doivent le limiter lorsque cela se produit, c’est-à-dire les recalculer uniquement lorsque cela est nécessaire. Pour ce faire, Excel prend en charge le mode Manuel. L’utilisateur peut sélectionner le mode via le système de menus Excel ou par programmation à l’aide de VBA, COM ou de l’API C.
  
Les tables de données sont des structures spéciales dans une feuille de calcul. Tout d’abord, l’utilisateur définit le calcul d’un résultat sur une feuille de calcul. Cela dépend d’une ou de deux entrées modifiables clé et d’autres paramètres. L’utilisateur peut ensuite créer une table de résultats pour un ensemble de valeurs pour l’une des valeurs clés, ou les deux. La table est créée à l’aide de l’**Assistant Table de données**. Une fois la table configurée, Excel transmet les entrées une par une au calcul et copie la valeur résultante dans la table. Étant donné qu’une ou deux entrées peuvent être utilisées, les tables de données peuvent comporter une ou deux dimensions.
  
Le recalcul des tables de données est légèrement différent :
  
- Le recalcul est géré de manière asynchrone pour le recalcul standard de classeur, c’est pourquoi les tables volumineuses peuvent nécessiter plus de temps de recalcul que le reste du classeur.
- Les références circulaires sont tolérées. Si le calcul utilisé pour obtenir le résultat dépend d’une ou de plusieurs valeurs de la table de données, Excel ne renvoie pas d’erreur pour la dépendance circulaire.
- Les tables de données n’utilisent pas le calcul à threads multiples.

Étant donné la manière dont Excel gère le recalcul de tables de données et le fait que les tables volumineuses dépendant de calculs complexes ou longs peuvent nécessiter un certain temps de calcul, Excel vous permet de désactiver le calcul automatique des tables de données. Pour ce faire, définissez le mode de calcul sur Automatique sauf dans les tables. Lorsque le calcul est dans ce mode, l’utilisateur recalcule les tables de données en appuyant sur F9 ou en réalisant une opération de programmation équivalente.
  
Excel propose des méthodes via lesquelles vous pouvez modifier le mode de recalcul et contrôler ce dernier. Ces méthodes ont été améliorées dans chaque version pour permettre un contrôle plus précis. Les fonctionnalités de l’API C à cet égard reflètent celles qui étaient disponibles dans la version 5 d’Excel, et ne fournissent donc pas le contrôle dont vous pouvez bénéficier en utilisant VBA dans les versions plus récentes.
  
Plus fréquemment utilisées lorsqu’Excel est en mode de calcul manuel, ces méthodes permettent le calcul sélectif des classeurs, des feuilles de calcul et des plages, le recalcul complet de tous les classeurs ouverts, et même la régénération de l’arborescence des dépendances et de la chaîne de calcul.
  
### <a name="range-calculation"></a>Calcul de la plage

Combinaison de touches : aucune
  
VBA : **Range.Calculate** (introduit dans Excel 2000, modifié dans Excel 2007) et **Range.CalculateRowMajorOrder** (introduit dans Excel 2007)
  
API C : non prise en charge
  
- **Mode Manuel**

    Permet de recalculer uniquement les cellules dans la plage donnée, qu’elles soient incorrectes ou non. Le comportement de la méthode **Range.Calculate** est modifié dans Excel 2007. Toutefois, l’ancien comportement est toujours pris en charge par la méthode **Range.CalculateRowMajorOrder**.

- **Modes Automatique ou Automatique sauf dans les tables**

    Permet de recalculer le classeur, mais n’impose pas le recalcul de la plage ou des cellules de la plage.

### <a name="active-worksheet-calculation"></a>Calcul de la feuille de calcul active

Combinaison de touches : MAJ + F9
  
VBA : **ActiveSheet.Calculate**
  
API C : **xlcCalculateDocument**
  
- **Tous les modes**

    Permet de recalculer les cellules marquées pour calcul dans la feuille de calcul active uniquement.

### <a name="specified-worksheet-calculation"></a>Calcul de la feuille de calcul indiquée

Combinaison de touches : aucune
  
VBA : **Worksheets(** référence **).Calculate**
  
API C : non prise en charge
  
- **Tous les modes**

Permet de recalculer les cellules incorrectes et leurs dépendances au sein de la feuille de calcul indiquée uniquement. La feuille de calcul porte le nom Référence, comme une chaîne ou le numéro d’index dans le classeur approprié.

Excel 2000 et les versions ultérieures proposent une propriété de feuille de calcul **Boolean**, la propriété **EnableCalculation**. Le fait de définir cette propriété sur **True** alors qu’elle était définie sur **False** rend toutes les cellules du classeur indiqué incorrectes. En mode automatique, cela déclenche également le recalcul de l’ensemble du classeur.

En mode Manuel, le code suivant génère le recalcul de la feuille active uniquement.

  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>Régénération de l’arborescence du classeur et recalcul forcé

Combinaison de touches : CTRL + ALT + MAJ + F9 (introduit dans Excel 2002)
  
VBA : **Workbooks(** référence **).ForceFullCalculation** (introduit dans Excel 2007)
  
API C : non prise en charge
  
- **Tous les modes**

    Entraîne la régénération de l’arborescence des dépendances et de la chaîne de calcul par Excel pour un classeur donné, et force le recalcul de toutes les cellules qui contiennent des formules.

### <a name="all-open-workbooks"></a>Tous les classeurs ouverts

Touche : F9
  
VBA : **Application.Calculate**
  
API C : **xlcCalculateNow**
  
- **Tous les modes**

    Permet de recalculer toutes les cellules qu’Excel a marquées comme incorrectes, c’est-à-dire dépendant de données volatiles ou modifiées, ainsi que les cellules marquées comme incorrectes par programmation. Si le mode de calcul est défini sur Automatique sauf dans les tables, cela calcule les tables qui nécessitent une mise à jour, ainsi que toutes les fonctions volatiles et leurs dépendances.

### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>Régénération d’arborescence de tous les classeurs ouverts et calcul forcé

Combinaison de touches : CTRL + ALT + F9
  
VBA : **Application.CalculateFull**
  
API C : non prise en charge
  
- **Tous les modes**

    Permet de recalculer toutes les cellules dans tous les classeurs ouverts. Si le mode de calcul est Automatique sauf dans les tables, cela force le recalcul des tables.

## <a name="see-also"></a>Voir aussi

[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
  
[Types de données utilisées par Excel](data-types-used-by-excel.md)
  
[Gestion de la mémoire dans Excel](memory-management-in-excel.md)
  
[Concepts de programmation Excel](excel-programming-concepts.md)
