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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782090"
---
# <a name="excel-recalculation"></a>Recalcul Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
L�utilisateur peut d�clencher le recalcul dans Microsoft�Excel de plusieurs fa�ons�:
  
- en saisissant de nouvelles donn�es (si Excel est en mode de recalcul automatique, d�crit plus loin dans cette rubrique)�;
    
- en demandant explicitement � Excel de recalculer l�int�gralit� ou la partie d�un classeur�;
    
- en supprimant ou ins�rant une ligne ou colonne�;
    
- en enregistrant un classeur alors que l�option **Recalcul avant l�enregistrement** est d�finie�; 
    
- en ex�cutant certaines actions de filtrage automatique�;
    
- en cliquant deux fois sur un s�parateur de ligne ou de colonne (en mode de calcul automatique)�;
    
- en ajoutant, modifiant ou supprimant un nom d�fini�;
    
- en renommant une feuille de calcul�;
    
- en modifiant la position d�une feuille de calcul li�e � d�autres feuilles de calcul�;
    
- en masquant ou affichant des lignes, mais pas des colonnes.
    
> [!NOTE]
> [!REMARQUE] Cette rubrique ne fait pas la diff�rence entre l�utilisateur appuyant sur une touche ou cliquant sur la souris, et les t�ches effectu�es par une commande ou une macro. L�utilisateur ex�cute la commande, ou fait quelque chose pour d�clencher l�ex�cution de la commande, de fa�on � ce que ce soit consid�r� comme une action de l�utilisateur. C�est pourquoi les termes ��l�utilisateur�� signifient �galement ��l�utilisateur, ou une commande ou processus ex�cut� par l�utilisateur��. 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>D�pendance, cellules incorrectes et cellules recalcul�es

Le calcul des feuilles de calcul dans Excel peut �tre consid�r� comme un processus � trois��tapes�:
  
1. Construction d�une arborescence des d�pendances
    
2. Construction d�une cha�ne de calcul
    
3. Recalcul de cellules
    
L�arborescence des d�pendances indique � Excel les cellules d�pendant d�autres cellules, ou de fa�on �quivalente, les cellules qui sont les ant�c�dents d�autres cellules. � partir de cette arborescence, Excel cr�e une cha�ne de calcul. Celle-ci r�pertorie toutes les cellules qui contiennent des formules dans l�ordre dans lequel elles doivent �tre calcul�es. Pendant le recalcul, Excel modifie cette cha�ne s�il rencontre une formule qui d�pend d�une cellule qui n�a pas encore �t� calcul�e. Dans ce cas, la cellule est calcul�e, et les cellules qui en d�pendent sont d�plac�es vers le bas de la cha�ne. Pour cette raison, les dur�es de calcul peuvent souvent �tre r�duites dans une feuille de calcul ayant juste �t� ouverte lors des premiers cycles de calcul.
  
Lorsqu�une modification structurelle est apport�e � un classeur, par exemple lorsqu�une nouvelle formule est saisie, Excel reconstruit l�arborescence des d�pendances et la cha�ne de calcul. Lors de la saisie de nouvelles donn�es ou formules, Excel marque toutes les cellules qui d�pendent de ces nouvelles donn�es comme n�cessitant un recalcul. Les cellules marqu�es de cette mani�re sont appel�es  *incorrectes*  . Toutes les cellules directement et indirectement d�pendantes sont marqu�es comme incorrectes. De ce fait, si B1 d�pend d�A1 et que C1 d�pend de B1, lorsque A1 est modifi�e, B1 et C1 sont marqu�es comme incorrectes. 
  
Si une cellule d�pend directement ou indirectement d�elle-m�me, Excel d�tecte la r�f�rence circulaire et avertit l�utilisateur. Il s�agit g�n�ralement d�une condition d�erreur que l�utilisateur doit r�soudre, et Excel fournit des outils de graphique et de navigation tr�s utiles pour aider l�utilisateur � trouver la source de la d�pendance circulaire. Dans certains cas, vous voudrez d�lib�r�ment que cette condition existe. Par exemple, vous souhaiterez peut-�tre ex�cuter un calcul it�ratif o� le point de d�part pour l�it�ration suivante est le r�sultat de l�it�ration pr�c�dente. Excel prend en charge le contr�le des calculs it�ratifs via la bo�te de dialogue des options de calcul.
  
Une fois que certaines cellules sont marqu�es comme incorrectes, lorsqu�un recalcul est effectu�, Excel r��value le contenu de chaque cellule incorrecte dans l�ordre d�termin� par la cha�ne de calcul. Dans l�exemple donn� pr�c�demment, cela signifie que B1 est calcul�e en premier lieu, suivie par C1. Ce calcul a lieu imm�diatement apr�s qu�Excel a termin� de marquer les cellules comme incorrectes si le mode de recalcul est automatique. Sinon, il se produit plus tard.
  
� partir de Microsoft�Excel�2002, l�objet **Range** dans Microsoft�Visual�Basic pour Applications (VBA) prend en charge une m�thode, **Range.Dirty**, qui indique les cellules n�cessitant un calcul. Lorsqu�elle est utilis�e conjointement � la m�thode **Range.Calculate** (voir la section suivante), elle permet le recalcul forc� de cellules dans une plage donn�e. Cela est utile lorsque vous effectuez un calcul limit� au cours d�une macro, o� le mode de calcul est d�fini sur manuel, afin d��viter la surcharge de calcul de cellules non li�es � la fonction de macro. Les m�thodes de calcul de plage ne sont pas disponibles via l�API�C. 
  
Dans Excel�2002 et versions ant�rieures, Excel a construit une cha�ne de calcul pour chaque feuille de calcul dans chaque classeur ouvert. Cela a g�n�r� une certaine complexit� dans la gestion des liens entre les feuilles de calcul, et a demand� de l�attention pour garantir un recalcul efficace. En particulier, dans Excel�2000, vous devez r�duire les d�pendances entre les classeurs et nommer les feuilles de calcul par ordre alphab�tique, afin que les feuilles d�pendant d�autres feuilles apparaissent apr�s les feuilles dont elles d�pendent.
  
Dans Excel 2007, la logique a �t� am�lior�e pour permettre le recalcul sur plusieurs threads afin que les sections de la cha�ne de calcul ne soient pas interd�pendantes et puissent �tre calcul�es en m�me temps. Vous pouvez configurer Excel pour utiliser plusieurs threads sur un ordinateur monoprocesseur ou un thread unique sur un ordinateur multiprocesseur ou multic�ur. 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>Fonctions d�finies par l�utilisateur (UDF) asynchrones

Lorsqu�un calcul rencontre une UDF asynchrone, il enregistre l��tat de la formule en cours, d�marre l�UDF et continue l��valuation des autres cellules. Lorsque le calcul termine l��valuation des cellules, Excel attend que les fonctions asynchrones se terminent s�il en existe encore en cours d�ex�cution. Lorsque les fonctions asynchrones g�n�rent des r�sultats, Excel termine la formule et ex�cute une nouvelle phase de calcul pour recalculer les cellules qui utilisent la cellule r�f�renc�e � la fonction asynchrone.
  
## <a name="volatile-and-non-volatile-functions"></a>Fonctions volatiles et non volatiles

Excel prend en charge le concept d�une fonction volatile, c�est-�-dire d�une fonction dont la valeur ne peut pas rester la m�me d�un moment � l�autre, m�me si aucun de ses arguments (si elle en a) n�a �t� modifi�. Excel r��value les cellules contenant des fonctions volatiles, ainsi que toutes les cellules d�pendantes, chaque fois qu�il r�alise un recalcul. C�est pourquoi un nombre trop �lev� de fonctions volatiles peut ralentir le recalcul. Utilisez-les avec parcimonie.
  
Les fonctions Excel suivantes sont volatiles�:
  
- **NOW**
    
- **TODAY**
    
- **RANDBETWEEN**
    
- **OFFSET**
    
- **INDIRECT**
    
- **INFO** (en fonction de ses arguments) 
    
- **CELL** (en fonction de ses arguments) 
    
- **SUMIF** (en fonction de ses arguments) 
    
Les VBA et l�API�C prennent en charge des m�thodes pour indiquer � Excel qu�une fonction d�finie par l�utilisateur (UDF) doit �tre trait�e comme une fonction volatile. � l�aide de VBA, l�UDF est d�clar�e comme volatile de la mani�re suivante.
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

Par d�faut, Excel suppose que les UDF�VBA ne sont pas volatiles. Excel apprend qu�une UDF est volatile lorsqu�il l�appelle pour la premi�re fois. Une UDF volatile peut �tre modifi�e en non volatile comme dans l�exemple suivant.
  
� l�aide de l�API�C, vous pouvez enregistrer une fonction�XLL comme �tant volatile avant son premier appel. Elle permet �galement d�activer et de d�sactiver le statut volatile d�une fonction de feuille de calcul.
  
Par d�faut, Excel g�re les UDF�XLL qui acceptent des arguments de plage et qui sont d�clar�es comme feuilles macro, �quivalent de volatiles. Vous pouvez d�sactiver cet �tat par d�faut � l�aide de la fonction **xlfVolatile** lorsque l�UDF est appel�e pour la premi�re fois. 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>Modes de calcul, commandes, recalcul s�lectif et tables de donn�es

Excel propose trois modes de calcul�:
  
- Automatique
    
- Automatique sauf dans les tables
    
- Manuel
    
Lorsque le calcul est d�fini sur Automatique, le recalcul se produit apr�s chaque entr�e de donn�es, et apr�s certains �v�nements tels que les exemples fournis dans la section pr�c�dente. Pour les classeurs tr�s volumineux, le temps de recalcul peut �tre si long que les utilisateurs doivent le limiter lorsque cela se produit, c�est-�-dire les recalculer uniquement lorsque cela est n�cessaire. Pour ce faire, Excel prend en charge le mode Manuel. L�utilisateur peut s�lectionner le mode via le syst�me de menus Excel ou par programmation � l�aide de VBA, COM ou de l�API�C.
  
Les tables de donn�es sont des structures sp�ciales dans une feuille de calcul. Tout d�abord, l�utilisateur d�finit le calcul d�un r�sultat sur une feuille de calcul. Cela d�pend d�une ou de deux entr�es modifiables cl� et d�autres param�tres. L�utilisateur peut ensuite cr�er une table de r�sultats pour un ensemble de valeurs pour l�une des valeurs cl�s, ou les deux. La table est cr��e � l�aide de l� **Assistant Table de donn�es**. Une fois la table configur�e, Excel transmet les entr�es une par une au calcul et copie la valeur r�sultante dans la table. �tant donn� qu�une ou deux entr�es peuvent �tre utilis�es, les tables de donn�es peuvent comporter une ou deux dimensions. 
  
Le recalcul des tables de donn�es est l�g�rement diff�rent�:
  
- Le recalcul est g�r� de mani�re asynchrone pour le recalcul standard de classeur, c�est pourquoi les tables volumineuses peuvent n�cessiter plus de temps de recalcul que le reste du classeur.
    
- Les r�f�rences circulaires sont tol�r�es. Si le calcul utilis� pour obtenir le r�sultat d�pend d�une ou de plusieurs valeurs de la table de donn�es, Excel ne renvoie pas d�erreur pour la d�pendance circulaire. 
    
�tant donn� la mani�re dont Excel g�re le recalcul de tables de donn�es et le fait que les tables volumineuses d�pendant de calculs complexes ou longs peuvent n�cessiter un certain temps de calcul, Excel vous permet de d�sactiver le calcul automatique des tables de donn�es. Pour ce faire, d�finissez le mode de calcul sur Automatique sauf dans les tables. Lorsque le calcul est dans ce mode, l�utilisateur recalcule les tables de donn�es en appuyant sur F9 ou en r�alisant une op�ration de programmation �quivalente.
  
Excel propose des m�thodes via lesquelles vous pouvez modifier le mode de recalcul et contr�ler ce dernier. Ces m�thodes ont �t� am�lior�es dans chaque version pour permettre un contr�le plus pr�cis. Les fonctionnalit�s de l�API�C � cet �gard refl�tent celles qui �taient disponibles dans la version�5 d�Excel, et ne fournissent donc pas le contr�le dont vous pouvez b�n�ficier en utilisant VBA dans les versions plus r�centes. 
  
Plus fr�quemment utilis�es lorsqu�Excel est en mode de calcul manuel, ces m�thodes permettent le calcul s�lectif des classeurs, des feuilles de calcul et des plages, le recalcul complet de tous les classeurs ouverts, et m�me la r�g�n�ration de l�arborescence des d�pendances et de la cha�ne de calcul.
  
### <a name="range-calculation"></a>Calcul de la plage

Combinaison de touches�: aucune
  
VBA�: **Range.Calculate** (introduit dans Excel�2000, modifi� dans Excel 2007) et **Range.CalculateRowMajorOrder** (introduit dans Excel 2007) 
  
API�C�: non prise en charge
  
- **Mode Manuel**
    
    Permet de recalculer uniquement les cellules dans la plage donn�e, qu�elles soient incorrectes ou non. Le comportement de la m�thode **Range.Calculate** est modifi� dans Excel 2007. Toutefois, l�ancien comportement est toujours pris en charge par la m�thode **Range.CalculateRowMajorOrder**. 
    
- **Modes Automatique ou Automatique sauf dans les tables**
    
    Permet de recalculer le classeur, mais n�impose pas le recalcul de la plage ou des cellules de la plage.
    
### <a name="active-worksheet-calculation"></a>Calcul de la feuille de calcul active

Combinaison de touches�: MAJ + F9
  
VBA�: **ActiveSheet.Calculate**
  
API�C�: **xlcCalculateDocument**
  
- **Tous les modes**
    
    Permet de recalculer les cellules marqu�es pour calcul dans la feuille de calcul active uniquement.
    
### <a name="specified-worksheet-calculation"></a>Calcul de la feuille de calcul indiqu�e

Combinaison de touches�: aucune
  
VBA�: **Worksheets(** r�f�rence **).Calculate**
  
API�C�: non prise en charge
  
- **Tous les modes**
    
    Permet de recalculer les cellules incorrectes et leurs d�pendances au sein de la feuille de calcul indiqu�e uniquement. La feuille de calcul porte le nom R�f�rence, comme une cha�ne ou le num�ro d�index dans le classeur appropri�.
    
    Excel�2000 et les versions ult�rieures proposent une propri�t� de feuille de calcul **Boolean**, la propri�t� **EnableCalculation**. Le fait de d�finir cette propri�t� sur **True** alors qu�elle �tait d�finie sur **False** rend toutes les cellules du classeur indiqu� incorrectes. En mode automatique, cela d�clenche �galement le recalcul de l�ensemble du classeur. 
    
    En mode Manuel, le code suivant g�n�re le recalcul de la feuille active uniquement.
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>R�g�n�ration de l�arborescence du classeur et recalcul forc�

Combinaison de touches�: CTRL + ALT + MAJ + F9 (introduit dans Excel�2002)
  
VBA�: **Workbooks(** r�f�rence **).ForceFullCalculation** (introduit dans Excel 2007) 
  
API�C�: non prise en charge
  
- **Tous les modes**
    
    Entra�ne la r�g�n�ration de l�arborescence des d�pendances et de la cha�ne de calcul par Excel pour un classeur donn�, et force le recalcul de toutes les cellules qui contiennent des formules.
    
### <a name="all-open-workbooks"></a>Tous les classeurs ouverts

Touche�: F9
  
VBA�: **Application.Calculate**
  
API�C�: **xlcCalculateNow**
  
- **Tous les modes**
    
    Permet de recalculer toutes les cellules qu�Excel a marqu�es comme incorrectes, c�est-�-dire d�pendant de donn�es volatiles ou modifi�es, ainsi que les cellules marqu�es comme incorrectes par programmation. Si le mode de calcul est d�fini sur Automatique sauf dans les tables, cela calcule les tables qui n�cessitent une mise � jour, ainsi que toutes les fonctions volatiles et leurs d�pendances.
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>R�g�n�ration d�arborescence de tous les classeurs ouverts et calcul forc�

Combinaison de touches�: CTRL + ALT + F9
  
VBA�: **Application.CalculateFull**
  
API�C�: non prise en charge
  
- **Tous les modes**
    
    Permet de recalculer toutes les cellules dans tous les classeurs ouverts. Si le mode de calcul est Automatique sauf dans les tables, cela force le recalcul des tables.
    
## <a name="see-also"></a>Voir aussi



[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
  
[Types de donn�es utilis�es par Excel](data-types-used-by-excel.md)
  
[Gestion de la m�moire dans Excel](memory-management-in-excel.md)
  
[Concepts de programmation Excel](excel-programming-concepts.md)

