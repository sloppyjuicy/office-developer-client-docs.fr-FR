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
# <a name="excel-recalculation"></a><span data-ttu-id="e9c14-104">Recalcul Excel</span><span class="sxs-lookup"><span data-stu-id="e9c14-104">Excel Recalculation</span></span>

 <span data-ttu-id="e9c14-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e9c14-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e9c14-106">L�utilisateur peut d�clencher le recalcul dans Microsoft�Excel de plusieurs fa�ons�:</span><span class="sxs-lookup"><span data-stu-id="e9c14-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="e9c14-107">en saisissant de nouvelles donn�es (si Excel est en mode de recalcul automatique, d�crit plus loin dans cette rubrique)�;</span><span class="sxs-lookup"><span data-stu-id="e9c14-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="e9c14-108">en demandant explicitement � Excel de recalculer l�int�gralit� ou la partie d�un classeur�;</span><span class="sxs-lookup"><span data-stu-id="e9c14-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="e9c14-109">en supprimant ou ins�rant une ligne ou colonne�;</span><span class="sxs-lookup"><span data-stu-id="e9c14-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="e9c14-110">en enregistrant un classeur alors que l�option **Recalcul avant l�enregistrement** est d�finie�;</span><span class="sxs-lookup"><span data-stu-id="e9c14-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="e9c14-111">en ex�cutant certaines actions de filtrage automatique�;</span><span class="sxs-lookup"><span data-stu-id="e9c14-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="e9c14-112">en cliquant deux fois sur un s�parateur de ligne ou de colonne (en mode de calcul automatique)�;</span><span class="sxs-lookup"><span data-stu-id="e9c14-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="e9c14-113">en ajoutant, modifiant ou supprimant un nom d�fini�;</span><span class="sxs-lookup"><span data-stu-id="e9c14-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="e9c14-114">en renommant une feuille de calcul�;</span><span class="sxs-lookup"><span data-stu-id="e9c14-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="e9c14-115">en modifiant la position d�une feuille de calcul li�e � d�autres feuilles de calcul�;</span><span class="sxs-lookup"><span data-stu-id="e9c14-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="e9c14-116">en masquant ou affichant des lignes, mais pas des colonnes.</span><span class="sxs-lookup"><span data-stu-id="e9c14-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e9c14-p101">[!REMARQUE] Cette rubrique ne fait pas la diff�rence entre l�utilisateur appuyant sur une touche ou cliquant sur la souris, et les t�ches effectu�es par une commande ou une macro. L�utilisateur ex�cute la commande, ou fait quelque chose pour d�clencher l�ex�cution de la commande, de fa�on � ce que ce soit consid�r� comme une action de l�utilisateur. C�est pourquoi les termes ��l�utilisateur�� signifient �galement ��l�utilisateur, ou une commande ou processus ex�cut� par l�utilisateur��.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p101">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro. The user runs the command, or does something to cause the command to run so that it is still considered a user action. Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="e9c14-120">D�pendance, cellules incorrectes et cellules recalcul�es</span><span class="sxs-lookup"><span data-stu-id="e9c14-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="e9c14-121">Le calcul des feuilles de calcul dans Excel peut �tre consid�r� comme un processus � trois��tapes�:</span><span class="sxs-lookup"><span data-stu-id="e9c14-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="e9c14-122">Construction d�une arborescence des d�pendances</span><span class="sxs-lookup"><span data-stu-id="e9c14-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="e9c14-123">Construction d�une cha�ne de calcul</span><span class="sxs-lookup"><span data-stu-id="e9c14-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="e9c14-124">Recalcul de cellules</span><span class="sxs-lookup"><span data-stu-id="e9c14-124">Recalculation of cells</span></span>
    
<span data-ttu-id="e9c14-p102">L�arborescence des d�pendances indique � Excel les cellules d�pendant d�autres cellules, ou de fa�on �quivalente, les cellules qui sont les ant�c�dents d�autres cellules. � partir de cette arborescence, Excel cr�e une cha�ne de calcul. Celle-ci r�pertorie toutes les cellules qui contiennent des formules dans l�ordre dans lequel elles doivent �tre calcul�es. Pendant le recalcul, Excel modifie cette cha�ne s�il rencontre une formule qui d�pend d�une cellule qui n�a pas encore �t� calcul�e. Dans ce cas, la cellule est calcul�e, et les cellules qui en d�pendent sont d�plac�es vers le bas de la cha�ne. Pour cette raison, les dur�es de calcul peuvent souvent �tre r�duites dans une feuille de calcul ayant juste �t� ouverte lors des premiers cycles de calcul.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p102">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others. From this tree, Excel constructs a calculation chain. The calculation chain lists all the cells that contain formulas in the order in which they should be calculated. During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated. In this case, the cell that is being calculated and its dependents are moved down the chain. For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="e9c14-p103">Lorsqu�une modification structurelle est apport�e � un classeur, par exemple lorsqu�une nouvelle formule est saisie, Excel reconstruit l�arborescence des d�pendances et la cha�ne de calcul. Lors de la saisie de nouvelles donn�es ou formules, Excel marque toutes les cellules qui d�pendent de ces nouvelles donn�es comme n�cessitant un recalcul. Les cellules marqu�es de cette mani�re sont appel�es  *incorrectes*  . Toutes les cellules directement et indirectement d�pendantes sont marqu�es comme incorrectes. De ce fait, si B1 d�pend d�A1 et que C1 d�pend de B1, lorsque A1 est modifi�e, B1 et C1 sont marqu�es comme incorrectes.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p103">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain. When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation. Cells that are marked in this way are known as  *dirty*  . All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="e9c14-p104">Si une cellule d�pend directement ou indirectement d�elle-m�me, Excel d�tecte la r�f�rence circulaire et avertit l�utilisateur. Il s�agit g�n�ralement d�une condition d�erreur que l�utilisateur doit r�soudre, et Excel fournit des outils de graphique et de navigation tr�s utiles pour aider l�utilisateur � trouver la source de la d�pendance circulaire. Dans certains cas, vous voudrez d�lib�r�ment que cette condition existe. Par exemple, vous souhaiterez peut-�tre ex�cuter un calcul it�ratif o� le point de d�part pour l�it�ration suivante est le r�sultat de l�it�ration pr�c�dente. Excel prend en charge le contr�le des calculs it�ratifs via la bo�te de dialogue des options de calcul.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p104">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user. This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency. In some cases, you might deliberately want this condition to exist. For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration. Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="e9c14-p105">Une fois que certaines cellules sont marqu�es comme incorrectes, lorsqu�un recalcul est effectu�, Excel r��value le contenu de chaque cellule incorrecte dans l�ordre d�termin� par la cha�ne de calcul. Dans l�exemple donn� pr�c�demment, cela signifie que B1 est calcul�e en premier lieu, suivie par C1. Ce calcul a lieu imm�diatement apr�s qu�Excel a termin� de marquer les cellules comme incorrectes si le mode de recalcul est automatique. Sinon, il se produit plus tard.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p105">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain. In the example given earlier, this means B1 is first, and then C1. This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="e9c14-p106">� partir de Microsoft�Excel�2002, l�objet **Range** dans Microsoft�Visual�Basic pour Applications (VBA) prend en charge une m�thode, **Range.Dirty**, qui indique les cellules n�cessitant un calcul. Lorsqu�elle est utilis�e conjointement � la m�thode **Range.Calculate** (voir la section suivante), elle permet le recalcul forc� de cellules dans une plage donn�e. Cela est utile lorsque vous effectuez un calcul limit� au cours d�une macro, o� le mode de calcul est d�fini sur manuel, afin d��viter la surcharge de calcul de cellules non li�es � la fonction de macro. Les m�thodes de calcul de plage ne sont pas disponibles via l�API�C.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p106">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation. When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range. This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function. Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="e9c14-p107">Dans Excel�2002 et versions ant�rieures, Excel a construit une cha�ne de calcul pour chaque feuille de calcul dans chaque classeur ouvert. Cela a g�n�r� une certaine complexit� dans la gestion des liens entre les feuilles de calcul, et a demand� de l�attention pour garantir un recalcul efficace. En particulier, dans Excel�2000, vous devez r�duire les d�pendances entre les classeurs et nommer les feuilles de calcul par ordre alphab�tique, afin que les feuilles d�pendant d�autres feuilles apparaissent apr�s les feuilles dont elles d�pendent.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p107">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook. This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation. In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="e9c14-p108">Dans Excel 2007, la logique a �t� am�lior�e pour permettre le recalcul sur plusieurs threads afin que les sections de la cha�ne de calcul ne soient pas interd�pendantes et puissent �tre calcul�es en m�me temps. Vous pouvez configurer Excel pour utiliser plusieurs threads sur un ordinateur monoprocesseur ou un thread unique sur un ordinateur multiprocesseur ou multic�ur.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p108">In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time. You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="e9c14-152">Fonctions d�finies par l�utilisateur (UDF) asynchrones</span><span class="sxs-lookup"><span data-stu-id="e9c14-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="e9c14-p109">Lorsqu�un calcul rencontre une UDF asynchrone, il enregistre l��tat de la formule en cours, d�marre l�UDF et continue l��valuation des autres cellules. Lorsque le calcul termine l��valuation des cellules, Excel attend que les fonctions asynchrones se terminent s�il en existe encore en cours d�ex�cution. Lorsque les fonctions asynchrones g�n�rent des r�sultats, Excel termine la formule et ex�cute une nouvelle phase de calcul pour recalculer les cellules qui utilisent la cellule r�f�renc�e � la fonction asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p109">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells. When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running. As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="e9c14-156">Fonctions volatiles et non volatiles</span><span class="sxs-lookup"><span data-stu-id="e9c14-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="e9c14-p110">Excel prend en charge le concept d�une fonction volatile, c�est-�-dire d�une fonction dont la valeur ne peut pas rester la m�me d�un moment � l�autre, m�me si aucun de ses arguments (si elle en a) n�a �t� modifi�. Excel r��value les cellules contenant des fonctions volatiles, ainsi que toutes les cellules d�pendantes, chaque fois qu�il r�alise un recalcul. C�est pourquoi un nombre trop �lev� de fonctions volatiles peut ralentir le recalcul. Utilisez-les avec parcimonie.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p110">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed. Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates. For this reason, too much reliance on volatile functions can make recalculation times slow. Use them sparingly.</span></span>
  
<span data-ttu-id="e9c14-161">Les fonctions Excel suivantes sont volatiles�:</span><span class="sxs-lookup"><span data-stu-id="e9c14-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="e9c14-162">**NOW**</span><span class="sxs-lookup"><span data-stu-id="e9c14-162">**NOW**</span></span>
    
- <span data-ttu-id="e9c14-163">**TODAY**</span><span class="sxs-lookup"><span data-stu-id="e9c14-163">**TODAY**</span></span>
    
- <span data-ttu-id="e9c14-164">**RANDBETWEEN**</span><span class="sxs-lookup"><span data-stu-id="e9c14-164">**RANDBETWEEN**</span></span>
    
- <span data-ttu-id="e9c14-165">**OFFSET**</span><span class="sxs-lookup"><span data-stu-id="e9c14-165">**OFFSET**</span></span>
    
- <span data-ttu-id="e9c14-166">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="e9c14-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="e9c14-167">**INFO** (en fonction de ses arguments)</span><span class="sxs-lookup"><span data-stu-id="e9c14-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="e9c14-168">**CELL** (en fonction de ses arguments)</span><span class="sxs-lookup"><span data-stu-id="e9c14-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="e9c14-169">**SUMIF** (en fonction de ses arguments)</span><span class="sxs-lookup"><span data-stu-id="e9c14-169">**SUMIF** (depending on its arguments)</span></span> 
    
<span data-ttu-id="e9c14-p111">Les VBA et l�API�C prennent en charge des m�thodes pour indiquer � Excel qu�une fonction d�finie par l�utilisateur (UDF) doit �tre trait�e comme une fonction volatile. � l�aide de VBA, l�UDF est d�clar�e comme volatile de la mani�re suivante.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p111">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile. By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="e9c14-p112">Par d�faut, Excel suppose que les UDF�VBA ne sont pas volatiles. Excel apprend qu�une UDF est volatile lorsqu�il l�appelle pour la premi�re fois. Une UDF volatile peut �tre modifi�e en non volatile comme dans l�exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p112">By default, Excel assumes that VBA UDFs are not volatile. Excel only learns that a UDF is volatile when it first calls it. A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="e9c14-p113">� l�aide de l�API�C, vous pouvez enregistrer une fonction�XLL comme �tant volatile avant son premier appel. Elle permet �galement d�activer et de d�sactiver le statut volatile d�une fonction de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p113">Using the C API, you can register an XLL function as volatile before its first call. It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="e9c14-p114">Par d�faut, Excel g�re les UDF�XLL qui acceptent des arguments de plage et qui sont d�clar�es comme feuilles macro, �quivalent de volatiles. Vous pouvez d�sactiver cet �tat par d�faut � l�aide de la fonction **xlfVolatile** lorsque l�UDF est appel�e pour la premi�re fois.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p114">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile. You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="e9c14-179">Modes de calcul, commandes, recalcul s�lectif et tables de donn�es</span><span class="sxs-lookup"><span data-stu-id="e9c14-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="e9c14-180">Excel propose trois modes de calcul�:</span><span class="sxs-lookup"><span data-stu-id="e9c14-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="e9c14-181">Automatique</span><span class="sxs-lookup"><span data-stu-id="e9c14-181">Automatic</span></span>
    
- <span data-ttu-id="e9c14-182">Automatique sauf dans les tables</span><span class="sxs-lookup"><span data-stu-id="e9c14-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="e9c14-183">Manuel</span><span class="sxs-lookup"><span data-stu-id="e9c14-183">Manual</span></span>
    
<span data-ttu-id="e9c14-p115">Lorsque le calcul est d�fini sur Automatique, le recalcul se produit apr�s chaque entr�e de donn�es, et apr�s certains �v�nements tels que les exemples fournis dans la section pr�c�dente. Pour les classeurs tr�s volumineux, le temps de recalcul peut �tre si long que les utilisateurs doivent le limiter lorsque cela se produit, c�est-�-dire les recalculer uniquement lorsque cela est n�cessaire. Pour ce faire, Excel prend en charge le mode Manuel. L�utilisateur peut s�lectionner le mode via le syst�me de menus Excel ou par programmation � l�aide de VBA, COM ou de l�API�C.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p115">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section. For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to. To enable this, Excel supports the manual mode. The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="e9c14-p116">Les tables de donn�es sont des structures sp�ciales dans une feuille de calcul. Tout d�abord, l�utilisateur d�finit le calcul d�un r�sultat sur une feuille de calcul. Cela d�pend d�une ou de deux entr�es modifiables cl� et d�autres param�tres. L�utilisateur peut ensuite cr�er une table de r�sultats pour un ensemble de valeurs pour l�une des valeurs cl�s, ou les deux. La table est cr��e � l�aide de l� **Assistant Table de donn�es**. Une fois la table configur�e, Excel transmet les entr�es une par une au calcul et copie la valeur r�sultante dans la table. �tant donn� qu�une ou deux entr�es peuvent �tre utilis�es, les tables de donn�es peuvent comporter une ou deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p116">Data tables are special structures in a worksheet. First, the user sets up the calculation of a result on a worksheet. This depends on one or two key changeable inputs and other parameters. The user can then create a table of results for a set of values for one or both of the key inputs. The table is created by using the **Data Table Wizard**. After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table. As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="e9c14-195">Le recalcul des tables de donn�es est l�g�rement diff�rent�:</span><span class="sxs-lookup"><span data-stu-id="e9c14-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="e9c14-196">Le recalcul est g�r� de mani�re asynchrone pour le recalcul standard de classeur, c�est pourquoi les tables volumineuses peuvent n�cessiter plus de temps de recalcul que le reste du classeur.</span><span class="sxs-lookup"><span data-stu-id="e9c14-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="e9c14-p117">Les r�f�rences circulaires sont tol�r�es. Si le calcul utilis� pour obtenir le r�sultat d�pend d�une ou de plusieurs valeurs de la table de donn�es, Excel ne renvoie pas d�erreur pour la d�pendance circulaire.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p117">Circular references are tolerated. If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 
    
<span data-ttu-id="e9c14-p118">�tant donn� la mani�re dont Excel g�re le recalcul de tables de donn�es et le fait que les tables volumineuses d�pendant de calculs complexes ou longs peuvent n�cessiter un certain temps de calcul, Excel vous permet de d�sactiver le calcul automatique des tables de donn�es. Pour ce faire, d�finissez le mode de calcul sur Automatique sauf dans les tables. Lorsque le calcul est dans ce mode, l�utilisateur recalcule les tables de donn�es en appuyant sur F9 ou en r�alisant une op�ration de programmation �quivalente.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p118">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables. To do this, set the calculation mode to Automatic except Data Tables. When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="e9c14-p119">Excel propose des m�thodes via lesquelles vous pouvez modifier le mode de recalcul et contr�ler ce dernier. Ces m�thodes ont �t� am�lior�es dans chaque version pour permettre un contr�le plus pr�cis. Les fonctionnalit�s de l�API�C � cet �gard refl�tent celles qui �taient disponibles dans la version�5 d�Excel, et ne fournissent donc pas le contr�le dont vous pouvez b�n�ficier en utilisant VBA dans les versions plus r�centes.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p119">Excel exposes methods through which you can alter the recalculation mode and control recalculation. These methods have been improved from version to version to allow for finer control. The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="e9c14-205">Plus fr�quemment utilis�es lorsqu�Excel est en mode de calcul manuel, ces m�thodes permettent le calcul s�lectif des classeurs, des feuilles de calcul et des plages, le recalcul complet de tous les classeurs ouverts, et m�me la r�g�n�ration de l�arborescence des d�pendances et de la cha�ne de calcul.</span><span class="sxs-lookup"><span data-stu-id="e9c14-205">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="e9c14-206">Calcul de la plage</span><span class="sxs-lookup"><span data-stu-id="e9c14-206">Range Calculation</span></span>

<span data-ttu-id="e9c14-207">Combinaison de touches�: aucune</span><span class="sxs-lookup"><span data-stu-id="e9c14-207">Keystroke: None</span></span>
  
<span data-ttu-id="e9c14-208">VBA�: **Range.Calculate** (introduit dans Excel�2000, modifi� dans Excel 2007) et **Range.CalculateRowMajorOrder** (introduit dans Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="e9c14-208">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="e9c14-209">API�C�: non prise en charge</span><span class="sxs-lookup"><span data-stu-id="e9c14-209">C API: Not supported</span></span>
  
- <span data-ttu-id="e9c14-210">**Mode Manuel**</span><span class="sxs-lookup"><span data-stu-id="e9c14-210">**Manual mode**</span></span>
    
    <span data-ttu-id="e9c14-p120">Permet de recalculer uniquement les cellules dans la plage donn�e, qu�elles soient incorrectes ou non. Le comportement de la m�thode **Range.Calculate** est modifi� dans Excel 2007. Toutefois, l�ancien comportement est toujours pris en charge par la m�thode **Range.CalculateRowMajorOrder**.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p120">Recalculates just the cells in the given range regardless of whether they are dirty or not. Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="e9c14-213">**Modes Automatique ou Automatique sauf dans les tables**</span><span class="sxs-lookup"><span data-stu-id="e9c14-213">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="e9c14-214">Permet de recalculer le classeur, mais n�impose pas le recalcul de la plage ou des cellules de la plage.</span><span class="sxs-lookup"><span data-stu-id="e9c14-214">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="e9c14-215">Calcul de la feuille de calcul active</span><span class="sxs-lookup"><span data-stu-id="e9c14-215">Active Worksheet Calculation</span></span>

<span data-ttu-id="e9c14-216">Combinaison de touches�: MAJ + F9</span><span class="sxs-lookup"><span data-stu-id="e9c14-216">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="e9c14-217">VBA�: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="e9c14-217">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="e9c14-218">API�C�: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="e9c14-218">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="e9c14-219">**Tous les modes**</span><span class="sxs-lookup"><span data-stu-id="e9c14-219">**All modes**</span></span>
    
    <span data-ttu-id="e9c14-220">Permet de recalculer les cellules marqu�es pour calcul dans la feuille de calcul active uniquement.</span><span class="sxs-lookup"><span data-stu-id="e9c14-220">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="e9c14-221">Calcul de la feuille de calcul indiqu�e</span><span class="sxs-lookup"><span data-stu-id="e9c14-221">Specified Worksheet Calculation</span></span>

<span data-ttu-id="e9c14-222">Combinaison de touches�: aucune</span><span class="sxs-lookup"><span data-stu-id="e9c14-222">Keystroke: None</span></span>
  
<span data-ttu-id="e9c14-223">VBA�: **Worksheets(** r�f�rence **).Calculate**</span><span class="sxs-lookup"><span data-stu-id="e9c14-223">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="e9c14-224">API�C�: non prise en charge</span><span class="sxs-lookup"><span data-stu-id="e9c14-224">C API: Not supported</span></span>
  
- <span data-ttu-id="e9c14-225">**Tous les modes**</span><span class="sxs-lookup"><span data-stu-id="e9c14-225">**All modes**</span></span>
    
    <span data-ttu-id="e9c14-p121">Permet de recalculer les cellules incorrectes et leurs d�pendances au sein de la feuille de calcul indiqu�e uniquement. La feuille de calcul porte le nom R�f�rence, comme une cha�ne ou le num�ro d�index dans le classeur appropri�.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p121">Recalculates the dirty cells and their dependents within the specified worksheet only. Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="e9c14-p122">Excel�2000 et les versions ult�rieures proposent une propri�t� de feuille de calcul **Boolean**, la propri�t� **EnableCalculation**. Le fait de d�finir cette propri�t� sur **True** alors qu�elle �tait d�finie sur **False** rend toutes les cellules du classeur indiqu� incorrectes. En mode automatique, cela d�clenche �galement le recalcul de l�ensemble du classeur.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p122">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property. Setting this to **True** from **False** dirties all cells in the specified worksheet. In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="e9c14-231">En mode Manuel, le code suivant g�n�re le recalcul de la feuille active uniquement.</span><span class="sxs-lookup"><span data-stu-id="e9c14-231">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="e9c14-232">R�g�n�ration de l�arborescence du classeur et recalcul forc�</span><span class="sxs-lookup"><span data-stu-id="e9c14-232">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="e9c14-233">Combinaison de touches�: CTRL + ALT + MAJ + F9 (introduit dans Excel�2002)</span><span class="sxs-lookup"><span data-stu-id="e9c14-233">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="e9c14-234">VBA�: **Workbooks(** r�f�rence **).ForceFullCalculation** (introduit dans Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="e9c14-234">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="e9c14-235">API�C�: non prise en charge</span><span class="sxs-lookup"><span data-stu-id="e9c14-235">C API: Not supported</span></span>
  
- <span data-ttu-id="e9c14-236">**Tous les modes**</span><span class="sxs-lookup"><span data-stu-id="e9c14-236">**All modes**</span></span>
    
    <span data-ttu-id="e9c14-237">Entra�ne la r�g�n�ration de l�arborescence des d�pendances et de la cha�ne de calcul par Excel pour un classeur donn�, et force le recalcul de toutes les cellules qui contiennent des formules.</span><span class="sxs-lookup"><span data-stu-id="e9c14-237">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="e9c14-238">Tous les classeurs ouverts</span><span class="sxs-lookup"><span data-stu-id="e9c14-238">All Open Workbooks</span></span>

<span data-ttu-id="e9c14-239">Touche�: F9</span><span class="sxs-lookup"><span data-stu-id="e9c14-239">Keystroke: F9</span></span>
  
<span data-ttu-id="e9c14-240">VBA�: **Application.Calculate**</span><span class="sxs-lookup"><span data-stu-id="e9c14-240">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="e9c14-241">API�C�: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="e9c14-241">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="e9c14-242">**Tous les modes**</span><span class="sxs-lookup"><span data-stu-id="e9c14-242">**All modes**</span></span>
    
    <span data-ttu-id="e9c14-p123">Permet de recalculer toutes les cellules qu�Excel a marqu�es comme incorrectes, c�est-�-dire d�pendant de donn�es volatiles ou modifi�es, ainsi que les cellules marqu�es comme incorrectes par programmation. Si le mode de calcul est d�fini sur Automatique sauf dans les tables, cela calcule les tables qui n�cessitent une mise � jour, ainsi que toutes les fonctions volatiles et leurs d�pendances.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p123">Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty. If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="e9c14-245">R�g�n�ration d�arborescence de tous les classeurs ouverts et calcul forc�</span><span class="sxs-lookup"><span data-stu-id="e9c14-245">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="e9c14-246">Combinaison de touches�: CTRL + ALT + F9</span><span class="sxs-lookup"><span data-stu-id="e9c14-246">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="e9c14-247">VBA�: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="e9c14-247">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="e9c14-248">API�C�: non prise en charge</span><span class="sxs-lookup"><span data-stu-id="e9c14-248">C API: Not supported</span></span>
  
- <span data-ttu-id="e9c14-249">**Tous les modes**</span><span class="sxs-lookup"><span data-stu-id="e9c14-249">**All modes**</span></span>
    
    <span data-ttu-id="e9c14-p124">Permet de recalculer toutes les cellules dans tous les classeurs ouverts. Si le mode de calcul est Automatique sauf dans les tables, cela force le recalcul des tables.</span><span class="sxs-lookup"><span data-stu-id="e9c14-p124">Recalculates all cells in all open workbooks. If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9c14-252">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9c14-252">See also</span></span>



[<span data-ttu-id="e9c14-253">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="e9c14-253">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="e9c14-254">Types de donn�es utilis�es par Excel</span><span class="sxs-lookup"><span data-stu-id="e9c14-254">Data Types Used by Excel</span></span>](data-types-used-by-excel.md)
  
[<span data-ttu-id="e9c14-255">Gestion de la m�moire dans Excel</span><span class="sxs-lookup"><span data-stu-id="e9c14-255">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="e9c14-256">Concepts de programmation Excel</span><span class="sxs-lookup"><span data-stu-id="e9c14-256">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

