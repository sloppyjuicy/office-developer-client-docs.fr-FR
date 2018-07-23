---
title: Recalcul Excel
manager: kelbow
ms.date: 03/09/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782090"
---
# <a name="excel-recalculation"></a>Recalcul Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
L’utilisateur peut déclencher le recalcul dans Microsoft Excel de plusieurs façons :
  
- en saisissant de nouvelles données (si Excel est en mode de recalcul automatique, décrit plus loin dans cette rubrique) ;
    
- en demandant explicitement à Excel de recalculer l’intégralité ou la partie d’un classeur ;
    
- en supprimant ou insérant une ligne ou colonne ;
    
- en enregistrant un classeur alors que l�option **Recalcul avant l�enregistrement** est d�finie�; 
    
- en exécutant certaines actions de filtrage automatique ;
    
- en cliquant deux fois sur un séparateur de ligne ou de colonne (en mode de calcul automatique) ;
    
- en ajoutant, modifiant ou supprimant un nom défini ;
    
- en renommant une feuille de calcul ;
    
- en modifiant la position d’une feuille de calcul liée à d’autres feuilles de calcul ;
    
- en masquant ou affichant des lignes, mais pas des colonnes.
    
> [!NOTE]
> Cette rubrique ne fait pas la différence entre l’utilisateur appuyant sur une touche ou cliquant sur la souris, et les tâches effectuées par une commande ou une macro. L’utilisateur exécute la commande, ou fait quelque chose pour déclencher l’exécution de la commande, de façon à ce que ce soit considéré comme une action de l’utilisateur. C’est pourquoi les termes « l’utilisateur » signifient également « l’utilisateur, ou une commande ou processus exécuté par l’utilisateur ». 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>Dépendance, cellules incorrectes et cellules recalculées

Le calcul des feuilles de calcul dans Excel peut être considéré comme un processus à trois étapes :
  
1. Construction d’une arborescence des dépendances
    
2. Construction d’une chaîne de calcul
    
3. Recalcul de cellules
    
L’arborescence des dépendances indique à Excel les cellules dépendant d’autres cellules, ou de façon équivalente, les cellules qui sont les antécédents d’autres cellules. À partir de cette arborescence, Excel crée une chaîne de calcul. Celle-ci répertorie toutes les cellules qui contiennent des formules dans l’ordre dans lequel elles doivent être calculées. Pendant le recalcul, Excel modifie cette chaîne s’il rencontre une formule qui dépend d’une cellule qui n’a pas encore été calculée. Dans ce cas, la cellule est calculée, et les cellules qui en dépendent sont déplacées vers le bas de la chaîne. Pour cette raison, les durées de calcul peuvent souvent être réduites dans une feuille de calcul ayant juste été ouverte lors des premiers cycles de calcul.
  
Lorsqu�une modification structurelle est apport�e � un classeur, par exemple lorsqu�une nouvelle formule est saisie, Excel reconstruit l�arborescence des d�pendances et la cha�ne de calcul. Lors de la saisie de nouvelles donn�es ou formules, Excel marque toutes les cellules qui d�pendent de ces nouvelles donn�es comme n�cessitant un recalcul. Les cellules marqu�es de cette mani�re sont appel�es  *incorrectes*  . Toutes les cellules directement et indirectement d�pendantes sont marqu�es comme incorrectes. De ce fait, si B1 d�pend d�A1 et que C1 d�pend de B1, lorsque A1 est modifi�e, B1 et C1 sont marqu�es comme incorrectes. 
  
Si une cellule dépend directement ou indirectement d’elle-même, Excel détecte la référence circulaire et avertit l’utilisateur. Il s’agit généralement d’une condition d’erreur que l’utilisateur doit résoudre, et Excel fournit des outils de graphique et de navigation très utiles pour aider l’utilisateur à trouver la source de la dépendance circulaire. Dans certains cas, vous voudrez délibérément que cette condition existe. Par exemple, vous souhaiterez peut-être exécuter un calcul itératif où le point de départ pour l’itération suivante est le résultat de l’itération précédente. Excel prend en charge le contrôle des calculs itératifs via la boîte de dialogue des options de calcul.
  
Une fois que certaines cellules sont marquées comme incorrectes, lorsqu’un recalcul est effectué, Excel réévalue le contenu de chaque cellule incorrecte dans l’ordre déterminé par la chaîne de calcul. Dans l’exemple donné précédemment, cela signifie que B1 est calculée en premier lieu, suivie par C1. Ce calcul a lieu immédiatement après qu’Excel a terminé de marquer les cellules comme incorrectes si le mode de recalcul est automatique. Sinon, il se produit plus tard.
  
� partir de Microsoft Excel 2002, l�objet **Range** dans Microsoft�Visual�Basic pour Applications (VBA) prend en charge une m�thode, **Range.Dirty**, qui indique les cellules n�cessitant un calcul. Lorsqu�elle est utilis�e conjointement � la m�thode **Range.Calculate** (voir la section suivante), elle permet le recalcul forc� de cellules dans une plage donn�e. Cela est utile lorsque vous effectuez un calcul limit� au cours d�une macro, o� le mode de calcul est d�fini sur manuel, afin d��viter la surcharge de calcul de cellules non li�es � la fonction de macro. Les m�thodes de calcul de plage ne sont pas disponibles via l�API C. 
  
Dans Excel 2002 et versions antérieures, Excel a construit une chaîne de calcul pour chaque feuille de calcul dans chaque classeur ouvert. Cela a généré une certaine complexité dans la gestion des liens entre les feuilles de calcul, et a demandé de l’attention pour garantir un recalcul efficace. En particulier, dans Excel 2000, vous devez réduire les dépendances entre les classeurs et nommer les feuilles de calcul par ordre alphabétique, afin que les feuilles dépendant d’autres feuilles apparaissent après les feuilles dont elles dépendent.
  
Dans Excel 2007, la logique a �t� am�lior�e pour permettre le recalcul sur plusieurs threads afin que les sections de la cha�ne de calcul ne soient pas interd�pendantes et puissent �tre calcul�es en m�me temps. Vous pouvez configurer Excel pour utiliser plusieurs threads sur un ordinateur monoprocesseur ou un thread unique sur un ordinateur multiprocesseur ou multic�ur. 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>Fonctions définies par l’utilisateur (UDF) asynchrones

Lorsqu’un calcul rencontre une UDF asynchrone, il enregistre l’état de la formule en cours, démarre l’UDF et continue l’évaluation des autres cellules. Lorsque le calcul termine l’évaluation des cellules, Excel attend que les fonctions asynchrones se terminent s’il en existe encore en cours d’exécution. Lorsque les fonctions asynchrones génèrent des résultats, Excel termine la formule et exécute une nouvelle phase de calcul pour recalculer les cellules qui utilisent la cellule référencée à la fonction asynchrone.
  
## <a name="volatile-and-non-volatile-functions"></a>Fonctions volatiles et non volatiles

Excel prend en charge le concept d’une fonction volatile, c’est-à-dire d’une fonction dont la valeur ne peut pas rester la même d’un moment à l’autre, même si aucun de ses arguments (si elle en a) n’a été modifié. Excel réévalue les cellules contenant des fonctions volatiles, ainsi que toutes les cellules dépendantes, chaque fois qu’il réalise un recalcul. C’est pourquoi un nombre trop élevé de fonctions volatiles peut ralentir le recalcul. Utilisez-les avec parcimonie.
  
Les fonctions Excel suivantes sont volatiles :
  
- **NOW**
    
- **TODAY**
    
- **RANDBETWEEN**
    
- **OFFSET**
    
- **INDIRECT**
    
- **INFO** (en fonction de ses arguments) 
    
- **CELL** (en fonction de ses arguments) 
    
- **SUMIF** (en fonction de ses arguments) 
    
Les VBA et l’API C prennent en charge des méthodes pour indiquer à Excel qu’une fonction définie par l’utilisateur (UDF) doit être traitée comme une fonction volatile. À l’aide de VBA, l’UDF est déclarée comme volatile de la manière suivante.
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

Par défaut, Excel suppose que les UDF VBA ne sont pas volatiles. Excel apprend qu’une UDF est volatile lorsqu’il l’appelle pour la première fois. Une UDF volatile peut être modifiée en non volatile comme dans l’exemple suivant.
  
À l’aide de l’API C, vous pouvez enregistrer une fonction XLL comme étant volatile avant son premier appel. Elle permet également d’activer et de désactiver le statut volatile d’une fonction de feuille de calcul.
  
Par d�faut, Excel g�re les UDF�XLL qui acceptent des arguments de plage et qui sont d�clar�es comme feuilles macro, �quivalent de volatiles. Vous pouvez d�sactiver cet �tat par d�faut � l�aide de la fonction **xlfVolatile** lorsque l�UDF est appel�e pour la premi�re fois. 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>Modes de calcul, commandes, recalcul sélectif et tables de données

Excel propose trois modes de calcul :
  
- Automatic
    
- Automatique sauf dans les tables
    
- Manual
    
Lorsque le calcul est défini sur Automatique, le recalcul se produit après chaque entrée de données, et après certains événements tels que les exemples fournis dans la section précédente. Pour les classeurs très volumineux, le temps de recalcul peut être si long que les utilisateurs doivent le limiter lorsque cela se produit, c’est-à-dire les recalculer uniquement lorsque cela est nécessaire. Pour ce faire, Excel prend en charge le mode Manuel. L’utilisateur peut sélectionner le mode via le système de menus Excel ou par programmation à l’aide de VBA, COM ou de l’API C.
  
Les tables de donn�es sont des structures sp�ciales dans une feuille de calcul. Tout d�abord, l�utilisateur d�finit le calcul d�un r�sultat sur une feuille de calcul. Cela d�pend d�une ou de deux entr�es modifiables cl� et d�autres param�tres. L�utilisateur peut ensuite cr�er une table de r�sultats pour un ensemble de valeurs pour l�une des valeurs cl�s, ou les deux. La table est cr��e � l�aide de l� **Assistant Table de donn�es**. Une fois la table configur�e, Excel transmet les entr�es une par une au calcul et copie la valeur r�sultante dans la table. �tant donn� qu�une ou deux entr�es peuvent �tre utilis�es, les tables de donn�es peuvent comporter une ou deux dimensions. 
  
Le recalcul des tables de données est légèrement différent :
  
- Le recalcul est géré de manière asynchrone pour le recalcul standard de classeur, c’est pourquoi les tables volumineuses peuvent nécessiter plus de temps de recalcul que le reste du classeur.
    
- Les références circulaires sont tolérées. Si le calcul utilisé pour obtenir le résultat dépend d’une ou de plusieurs valeurs de la table de données, Excel ne renvoie pas d’erreur pour la dépendance circulaire. 
    
Étant donné la manière dont Excel gère le recalcul de tables de données et le fait que les tables volumineuses dépendant de calculs complexes ou longs peuvent nécessiter un certain temps de calcul, Excel vous permet de désactiver le calcul automatique des tables de données. Pour ce faire, définissez le mode de calcul sur Automatique sauf dans les tables. Lorsque le calcul est dans ce mode, l’utilisateur recalcule les tables de données en appuyant sur F9 ou en réalisant une opération de programmation équivalente.
  
Excel propose des méthodes via lesquelles vous pouvez modifier le mode de recalcul et contrôler ce dernier. Ces méthodes ont été améliorées dans chaque version pour permettre un contrôle plus précis. Les fonctionnalités de l’API C à cet égard reflètent celles qui étaient disponibles dans la version 5 d’Excel, et ne fournissent donc pas le contrôle dont vous pouvez bénéficier en utilisant VBA dans les versions plus récentes. 
  
Plus fréquemment utilisées lorsqu’Excel est en mode de calcul manuel, ces méthodes permettent le calcul sélectif des classeurs, des feuilles de calcul et des plages, le recalcul complet de tous les classeurs ouverts, et même la régénération de l’arborescence des dépendances et de la chaîne de calcul.
  
### <a name="range-calculation"></a>Calcul de la plage

Combinaison de touches : aucune
  
VBA : **Range.Calculate** (introduit dans Excel 2000, modifi� dans Excel 2007) et **Range.CalculateRowMajorOrder** (introduit dans Excel 2007) 
  
API C : non prise en charge
  
- **Mode Manuel**
    
    Permet de recalculer uniquement les cellules dans la plage donn�e, qu�elles soient incorrectes ou non. Le comportement de la m�thode **Range.Calculate** est modifi� dans Excel 2007. Toutefois, l�ancien comportement est toujours pris en charge par la m�thode **Range.CalculateRowMajorOrder**. 
    
- **Modes Automatique ou Automatique sauf dans les tables**
    
    Permet de recalculer le classeur, mais n’impose pas le recalcul de la plage ou des cellules de la plage.
    
### <a name="active-worksheet-calculation"></a>Calcul de la feuille de calcul active

Combinaison de touches : MAJ + F9
  
VBA : **ActiveSheet.Calculate**
  
API C : **xlcCalculateDocument**
  
- **Tous les modes**
    
    Permet de recalculer les cellules marquées pour calcul dans la feuille de calcul active uniquement.
    
### <a name="specified-worksheet-calculation"></a>Calcul de la feuille de calcul indiquée

Combinaison de touches : aucune
  
VBA : **Worksheets(** r�f�rence **).Calculate**
  
API C : non prise en charge
  
- **Tous les modes**
    
    Permet de recalculer les cellules incorrectes et leurs dépendances au sein de la feuille de calcul indiquée uniquement. La feuille de calcul porte le nom Référence, comme une chaîne ou le numéro d’index dans le classeur approprié.
    
    Excel 2000 et les versions ult�rieures proposent une propri�t� de feuille de calcul **Boolean**, la propri�t� **EnableCalculation**. Le fait de d�finir cette propri�t� sur **True** alors qu�elle �tait d�finie sur **False** rend toutes les cellules du classeur indiqu� incorrectes. En mode automatique, cela d�clenche �galement le recalcul de l�ensemble du classeur. 
    
    En mode Manuel, le code suivant génère le recalcul de la feuille active uniquement.
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>Régénération de l’arborescence du classeur et recalcul forcé

Combinaison de touches : CTRL + ALT + MAJ + F9 (introduit dans Excel 2002)
  
VBA : **Workbooks(** r�f�rence **).ForceFullCalculation** (introduit dans Excel 2007) 
  
API C : non prise en charge
  
- **Tous les modes**
    
    Entraîne la régénération de l’arborescence des dépendances et de la chaîne de calcul par Excel pour un classeur donné, et force le recalcul de toutes les cellules qui contiennent des formules.
    
### <a name="all-open-workbooks"></a>Tous les classeurs ouverts

Touche : F9
  
VBA : **Application.Calculate**
  
API C : **xlcCalculateNow**
  
- **Tous les modes**
    
    Permet de recalculer toutes les cellules qu’Excel a marquées comme incorrectes, c’est-à-dire dépendant de données volatiles ou modifiées, ainsi que les cellules marquées comme incorrectes par programmation. Si le mode de calcul est défini sur Automatique sauf dans les tables, cela calcule les tables qui nécessitent une mise à jour, ainsi que toutes les fonctions volatiles et leurs dépendances.
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>Régénération d’arborescence de tous les classeurs ouverts et calcul forcé

Combinaison de touches : CTRL + ALT + F9
  
VBA : **Application.CalculateFull**
  
API C : non prise en charge
  
- **Tous les modes**
    
    Permet de recalculer toutes les cellules dans tous les classeurs ouverts. Si le mode de calcul est Automatique sauf dans les tables, cela force le recalcul des tables.
    
## <a name="see-also"></a>Voir aussi



[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
  
[Types de donn�es utilis�es par Excel](data-types-used-by-excel.md)
  
[Gestion de la m�moire dans Excel](memory-management-in-excel.md)
  
[Concepts de programmation Excel](excel-programming-concepts.md)

