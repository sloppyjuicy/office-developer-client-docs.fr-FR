---
title: Recalcul multithread dans Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- thread-safe cells [excel 2007],multithreading in Excel,concurrent tasks [Excel 2007],thread-safe functions [Excel 2007],multithreaded recalculation [Excel 2007],MTR [Excel 2007],XLL functions [Excel 2007], registering as thread safe,recalculation [Excel 2007], multithreaded,memory contention [Excel 2007],registering XLL functions as thread safe [Excel 2007],unsafe functions [Excel 2007]
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: f0b6f3d7310cac6d141fc74652a3333f70bda8e9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720708"
---
# <a name="multithreaded-recalculation-in-excel"></a><span data-ttu-id="b9144-104">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="b9144-104">Multithreaded recalculation in Excel</span></span>

<span data-ttu-id="b9144-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b9144-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b9144-p101">Microsoft Office Excel 2007 a �t� la premi�re version d�Excel � utiliser le recalcul multithread (MTR) de feuilles de calcul. Vous pouvez configurer Excel pour utiliser jusqu�� 1�024�threads simultan�s lors du recalcul, quel que soit le nombre de processeurs ou de c�urs de processeur pr�sents sur l�ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b9144-p101">Microsoft Office Excel 2007 was the first version of Excel to use multithreaded recalculation (MTR) of worksheets. You can configure Excel to use up to 1024 concurrent threads when recalculating, regardless of the number of processors or processor cores on the computer.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b9144-108">Il existe une surcharge de systéme d�exploitation li�e � chaque thread. �vitez donc de configurer Excel pour qu�il utilise plus de threads que n�cessaire.</span><span class="sxs-lookup"><span data-stu-id="b9144-108">There is an operating system overhead associated with each thread, so you should not configure Excel to use more threads than you need.</span></span> 
  
<span data-ttu-id="b9144-109">Si l�ordinateur dispose de plusieurs processeurs ou c�urs de processeur, le systéme d�exploitation a la responsabilit� d�allouer les threads aux processeurs de la mani�re la plus efficace.</span><span class="sxs-lookup"><span data-stu-id="b9144-109">If the computer has multiple processors or processor cores, the operating system takes responsibility for allocating the threads to the processors in the most efficient way.</span></span>
  
## <a name="excel-mtr-overview"></a><span data-ttu-id="b9144-110">Vue d’ensemble du recalcul multithread Excel</span><span class="sxs-lookup"><span data-stu-id="b9144-110">Excel MTR overview</span></span>

<span data-ttu-id="b9144-p102">Excel tente d�identifier des parties de la cha�ne de calcul pouvant �tre recalcul�es simultan�ment sur diff�rents threads. L�arborescence tr�s simple suivante (o� x ? y signifie que y d�pend uniquement de x) en pr�sente un exemple.</span><span class="sxs-lookup"><span data-stu-id="b9144-p102">Excel tries to identify parts of the calculation chain that can be recalculated concurrently on different threads. The following very simple tree (where x ← y means y only depends on x) shows an example of this.</span></span>
  
<span data-ttu-id="b9144-113">**Figure 1. Calcul simultané sur différents threads**</span><span class="sxs-lookup"><span data-stu-id="b9144-113">**Figure 1. Calculating concurrently on different threads**</span></span>

<span data-ttu-id="b9144-114">![Calcul simultané sur différents threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calcul simultané sur différents threads")</span><span class="sxs-lookup"><span data-stu-id="b9144-114">![Calculating concurrently on different threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculating concurrently on different threads")</span></span>
  
<span data-ttu-id="b9144-115">Apr�s avoir calcul� A1, A2 et A3 peuvent �tre calcul�es sur un thread, tandis que B1 et C1 peuvent �tre calcul�es sur un autre, en supposant que toutes les cellules sont thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b9144-115">After A1 is calculated, A2 and then A3 can be calculated on one thread, while B1 and then C1 can be calculated on another, assuming all the cells are thread safe.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b9144-p103">Le terme cellule thread-safe d�signe une cellule contenant uniquement des fonctions thread-safe. Les �l�ments thread-safe et non thread-safe sont d�taill�s [�l�ments consid�r�s comme thread-safe ou non par Excel](#xl2007xllsdk_threadsafe).</span><span class="sxs-lookup"><span data-stu-id="b9144-p103">The term thread-safe cell means a cell that only contains thread-safe functions. What is and is not thread-safe is detailed [What Is and Is Not Considered Thread Safe by Excel](#xl2007xllsdk_threadsafe).</span></span> 
  
<span data-ttu-id="b9144-p104">Les classeurs les plus pratiques contiennent des arborescences des d�pendances beaucoup plus complexes que celle de cet exemple. En outre, la dur�e de recalcul d�une cellule ne peut �tre connue qu�une fois le recalcul termin�, et peut varier consid�rablement selon les arguments des fonctions. Pour obtenir les meilleurs r�sultats, Excel essaie d�am�liorer l�ordre de calcul pour chaque calcul jusqu�� ce qu�aucune optimisation suppl�mentaire ne soit possible.</span><span class="sxs-lookup"><span data-stu-id="b9144-p104">Most practical workbooks contain far more complex dependency trees than this example. Moreover, the recalculation time of a cell cannot be known until a calculation is done and can vary greatly depending on the functions' arguments. To obtain the best results, Excel tries to improve the calculation order on every calculation until no further optimization is possible.</span></span>
  
<span data-ttu-id="b9144-121">Excel utilise un thread principal unique � ex�cuter, ou ex�cute les �l�ments suivants :</span><span class="sxs-lookup"><span data-stu-id="b9144-121">Excel uses a single main thread to run or execute the following:</span></span>
  
- <span data-ttu-id="b9144-122">commandes int�gr�es�;</span><span class="sxs-lookup"><span data-stu-id="b9144-122">Built-in commands</span></span>
    
- <span data-ttu-id="b9144-123">Commandes XLL</span><span class="sxs-lookup"><span data-stu-id="b9144-123">XLL commands</span></span>
    
- <span data-ttu-id="b9144-124">Fonctions de l’interface du gestionnaire de compléments XLL (fonction **xlAutoOpen** et ainsi de suite)</span><span class="sxs-lookup"><span data-stu-id="b9144-124">XLL Add-in Manager interface functions (**xlAutoOpen** function, and so on)</span></span> 
    
- <span data-ttu-id="b9144-125">Commandes Microsoft Visual Basic pour Applications (VBA) définies par l’utilisateur (souvent appelées macros)</span><span class="sxs-lookup"><span data-stu-id="b9144-125">Microsoft Visual Basic for Applications (VBA) user-defined commands (often referred to as macros)</span></span>
    
- <span data-ttu-id="b9144-126">fonctions VBA d�finies par l�utilisateur�;</span><span class="sxs-lookup"><span data-stu-id="b9144-126">VBA user-defined functions</span></span>
    
- <span data-ttu-id="b9144-127">fonctions de feuille de calcul non thread-safe int�gr�es (voir la section suivante pour obtenir la liste)�;</span><span class="sxs-lookup"><span data-stu-id="b9144-127">Built-in thread-unsafe worksheet functions (see the next section for a list)</span></span>
    
- <span data-ttu-id="b9144-128">fonctions et commandes d�finies par l�utilisateur de feuille de macro XLM�;</span><span class="sxs-lookup"><span data-stu-id="b9144-128">XLM macro sheet user-defined commands and functions</span></span>
    
- <span data-ttu-id="b9144-129">fonctions et commandes de compl�ment COM�;</span><span class="sxs-lookup"><span data-stu-id="b9144-129">COM add-in commands and functions</span></span>
    
- <span data-ttu-id="b9144-130">fonctions et op�rateurs dans des expressions de mise en forme conditionnelles�;</span><span class="sxs-lookup"><span data-stu-id="b9144-130">Functions and operators within conditional formatting expressions</span></span>
    
- <span data-ttu-id="b9144-131">fonctions et op�rateurs dans des d�finitions de nom d�fini utilis�es dans les formules de feuille de calcul�;</span><span class="sxs-lookup"><span data-stu-id="b9144-131">Functions and operators within defined name definitions used in worksheet formulas</span></span>
    
- <span data-ttu-id="b9144-132">�valuation forc�e d�une expression dans la zone d��dition de formule � l�aide de la touche **F9**.</span><span class="sxs-lookup"><span data-stu-id="b9144-132">The forced evaluation of an expression in the formula-edit box using the **F9** key</span></span> 
    
<span data-ttu-id="b9144-p105">Toutes les formules de feuille de calcul, que les fonctions soient thread-safe ou non, sont �valu�es sur le thread principal, sauf si Excel est configur� pour utiliser plusieurs threads. Lorsque l�utilisateur indique que plusieurs threads doivent �tre utilis�s, les threads suppl�mentaires sont utilis�s pour les cellules thread-safe. Notez que le thread principal peut encore �tre utilis� pour les cellules thread-safe lorsque cela est pertinent du point de vue d�un �quilibreur de charge.</span><span class="sxs-lookup"><span data-stu-id="b9144-p105">All worksheet formulas, regardless of whether the functions are thread safe or not, are evaluated on the main thread unless Excel is configured to use more than one thread. When the user specifies that more than one thread should be used, the additional threads are used for thread-safe cells. Note that the main thread may still be used for thread-safe cells when it makes sense from a load-balancing point of view.</span></span>
  
<span data-ttu-id="b9144-136">Il est int�ressant de rev�rifier qu�Excel n�ex�cute pas plus d�une commande � la fois, de fa�on � ce que vous n�ayez pas besoin d�utiliser les m�mes pr�cautions que lorsque vous �crivez des fonctions thread-safe, telles que l�utilisation de la m�moire locale de thread et des sections critiques.</span><span class="sxs-lookup"><span data-stu-id="b9144-136">It is worth restating that Excel does not run more than one command at once, so you do not need to employ the same precautions as when you are writing thread-safe functions, such as the use of thread-local memory and critical sections.</span></span>
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a><span data-ttu-id="b9144-137">Éléments considérés comme thread-safe ou non par Excel</span><span class="sxs-lookup"><span data-stu-id="b9144-137">What is and is not considered thread safe by Excel</span></span>
<span data-ttu-id="b9144-138"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="b9144-138"><a name="xl2007xllsdk_threadsafe"> </a></span></span>

<span data-ttu-id="b9144-139">Pour Excel, seuls les �l�ments suivants sont thread-safe :</span><span class="sxs-lookup"><span data-stu-id="b9144-139">Excel only considers the following as thread safe:</span></span>
  
- <span data-ttu-id="b9144-140">tous les op�rateurs unaires et binaires dans Excel�;</span><span class="sxs-lookup"><span data-stu-id="b9144-140">All unary and binary operators in Excel.</span></span>
    
- <span data-ttu-id="b9144-141">presque toutes les fonctions de feuille de calcul int�gr�es � partir d�Excel 2007 (voir la liste des exceptions)�;</span><span class="sxs-lookup"><span data-stu-id="b9144-141">Almost all built-in worksheet functions starting in Excel 2007 (see exceptions list)</span></span>
    
- <span data-ttu-id="b9144-142">les fonctions de compl�ment XLL qui ont �t� explicitement enregistr�es comme thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b9144-142">XLL add-in functions that have been explicitly registered as thread-safe.</span></span>
    
<span data-ttu-id="b9144-143">Les fonctions de feuille de calcul int�gr�es qui ne sont pas thread-safe sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b9144-143">The built-in worksheet functions that are not thread safe are:</span></span>
  
- <span data-ttu-id="b9144-144">**PHONETIC**</span><span class="sxs-lookup"><span data-stu-id="b9144-144">**PHONETIC**</span></span>
    
- <span data-ttu-id="b9144-145">**CELL** lorsque l�argument « format » ou « adress » est utilis�</span><span class="sxs-lookup"><span data-stu-id="b9144-145">**CELL** when either the "format" or "address" argument is used</span></span> 
    
- <span data-ttu-id="b9144-146">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="b9144-146">**INDIRECT**</span></span>
    
- <span data-ttu-id="b9144-147">**GETPIVOTDATA**</span><span class="sxs-lookup"><span data-stu-id="b9144-147">**GETPIVOTDATA**</span></span>
    
- <span data-ttu-id="b9144-148">**CUBEMEMBER**</span><span class="sxs-lookup"><span data-stu-id="b9144-148">**CUBEMEMBER**</span></span>
    
- <span data-ttu-id="b9144-149">**CUBEVALUE**</span><span class="sxs-lookup"><span data-stu-id="b9144-149">**CUBEVALUE**</span></span>
    
- <span data-ttu-id="b9144-150">**CUBEMEMBERPROPERTY**</span><span class="sxs-lookup"><span data-stu-id="b9144-150">**CUBEMEMBERPROPERTY**</span></span>
    
- <span data-ttu-id="b9144-151">**CUBESET**</span><span class="sxs-lookup"><span data-stu-id="b9144-151">**CUBESET**</span></span>
    
- <span data-ttu-id="b9144-152">**CUBERANKEDMEMBER**</span><span class="sxs-lookup"><span data-stu-id="b9144-152">**CUBERANKEDMEMBER**</span></span>
    
- <span data-ttu-id="b9144-153">**CUBEKPIMEMBER**</span><span class="sxs-lookup"><span data-stu-id="b9144-153">**CUBEKPIMEMBER**</span></span>
    
- <span data-ttu-id="b9144-154">**CUBESETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="b9144-154">**CUBESETCOUNT**</span></span>
    
- <span data-ttu-id="b9144-155">**ADRESS** où figure le cinquième paramètre (sheet_name)</span><span class="sxs-lookup"><span data-stu-id="b9144-155">**ADDRESS** where the fifth parameter (the sheet_name) is given</span></span> 
    
- <span data-ttu-id="b9144-156">Toute fonction de base de données (**DSUM**, **DAVERAGE**, et ainsi de suite) qui fait référence à un tableau croisé dynamique</span><span class="sxs-lookup"><span data-stu-id="b9144-156">Any database function (**DSUM**, **DAVERAGE**, and so on) that refers to a pivot table</span></span>
    
- <span data-ttu-id="b9144-157">**ERROR.TYPE**</span><span class="sxs-lookup"><span data-stu-id="b9144-157">**ERROR.TYPE**</span></span>
    
- <span data-ttu-id="b9144-158">**HYPERLINK**</span><span class="sxs-lookup"><span data-stu-id="b9144-158">**HYPERLINK**</span></span>
    
<span data-ttu-id="b9144-159">Pour �tre explicites, les �l�ments suivants sont consid�r�s comme non s�curis�s :</span><span class="sxs-lookup"><span data-stu-id="b9144-159">To be explicit, the following are considered to be unsafe:</span></span>
  
- <span data-ttu-id="b9144-160">fonctions VBA d�finies par l�utilisateur�;</span><span class="sxs-lookup"><span data-stu-id="b9144-160">VBA user-defined functions</span></span>
    
- <span data-ttu-id="b9144-161">fonctions d�finies par l�utilisateur de compl�ment COM�;</span><span class="sxs-lookup"><span data-stu-id="b9144-161">COM add-in user-defined functions</span></span>
    
- <span data-ttu-id="b9144-162">fonctions d�finies par l�utilisateur de feuille macro XLM�;</span><span class="sxs-lookup"><span data-stu-id="b9144-162">XLM macro-sheet user-defined functions</span></span>
    
- <span data-ttu-id="b9144-163">fonctions de compl�ment XLL non enregistr�es explicitement comme thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b9144-163">XLL add-in functions not explicitly registered as thread safe</span></span>
    
<span data-ttu-id="b9144-164">Les cons�quences sont que les op�rations et fonctions suivantes ne sont pas thread-safe, et �chouent si elles sont appel�es � partir d�une fonction�XLL enregistr�e en tant que thread-safe :</span><span class="sxs-lookup"><span data-stu-id="b9144-164">The implications are that the following operations and functions are not thread-safe, and fail if they are called from an XLL function registered as thread safe:</span></span>
  
- <span data-ttu-id="b9144-165">Appels vers les fonctions d’information XLM, par exemple, **xlfGetCell** (**GET.CELL**).</span><span class="sxs-lookup"><span data-stu-id="b9144-165">Calls to XLM information functions, for example, **xlfGetCell** (**GET.CELL**).</span></span>
    
- <span data-ttu-id="b9144-166">Appels vers des éléments **xlfSetName** (**SET.NAME**) pour définir ou supprimer des noms XLL internes.</span><span class="sxs-lookup"><span data-stu-id="b9144-166">Calls to **xlfSetName** (**SET.NAME**) to define or delete XLL-internal names.</span></span>
    
- <span data-ttu-id="b9144-167">Appels vers les fonctions définies par l’utilisateur comme non thread-safe à l’aide d’**xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="b9144-167">Calls to thread-unsafe user-defined functions using **xlUDF**.</span></span>
    
- <span data-ttu-id="b9144-168">appels vers la fonction [xlfEvaluate](xlfevaluate.md) pour des expressions contenant des fonctions non thread-safe ou des noms d�finis dont les d�finitions contiennent des fonctions non thread-safe�;</span><span class="sxs-lookup"><span data-stu-id="b9144-168">Calls to the [xlfEvaluate](xlfevaluate.md) function for expressions that contain thread-unsafe functions or that contain defined names whose definitions contain thread-unsafe functions.</span></span> 
    
- <span data-ttu-id="b9144-169">appels vers la fonction [xlAbort](xlabort.md) pour effacer une condition d�arr�t�;</span><span class="sxs-lookup"><span data-stu-id="b9144-169">Calls to the [xlAbort](xlabort.md) function to clear a break condition.</span></span> 
    
- <span data-ttu-id="b9144-170">appels vers la fonction [xlCoerce](xlcoerce.md) pour obtenir la valeur d�une référence de cellule non calcul�e.</span><span class="sxs-lookup"><span data-stu-id="b9144-170">Calls to the [xlCoerce](xlcoerce.md) function to get the value of an uncalculated cell reference.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="b9144-171">Les fonctions de feuille de calcul�XLL ne sont pas autoris�es � appeler les commandes d�API C, par exemple **xlcSave**, qu�elles aient �t� enregistr�es en tant que thread-safe ou non.</span><span class="sxs-lookup"><span data-stu-id="b9144-171">XLL worksheet functions are not permitted to call C API commands, for example, **xlcSave**, regardless of whether they have been registered as thread safe or not.</span></span> 
  
<span data-ttu-id="b9144-p106">�tant donn� que les fonctions�XLL d�clar�es comme thread-safe ne peuvent pas appeler les fonctions d�informations XLM ou les cellules non calcul�es de référence, Excel n�autorise pas les fonctions�XLL qui sont enregistr�es comme des �quivalents de feuille macro, pouvant aussi �tre enregistr�es en tant que thread-safe. Par cons�quent, la tentative d�obtention de la valeur d�une référence de cellule non calcul�e � l�aide de l��l�ment **xlCoerce** �choue avec une erreur **xlretUncalced**. L�appel d�une fonction d�information XLM �choue avec une erreur **xlretFailed**. Les autres points r�pertori�s pr�c�demment �chouent avec un code d�erreur introduit dans l�API C Excel : **xlretNotThreadSafe**.</span><span class="sxs-lookup"><span data-stu-id="b9144-p106">Given that XLL functions declared as thread safe cannot call XLM information functions or reference uncalculated cells, Excel does not permit XLL functions that are registered as macro sheet equivalents to also be registered as thread safe. Therefore attempting to get the value of an uncalculated cell reference using **xlCoerce** fails with an **xlretUncalced** error. Calling an XLM information function fails with an **xlretFailed** error. The other points listed previously fail with an error code introduced in the Excel C API: **xlretNotThreadSafe**.</span></span> 
  
<span data-ttu-id="b9144-176">Les fonctions de rappel concernant uniquement l�API C sont toutes thread-safe :</span><span class="sxs-lookup"><span data-stu-id="b9144-176">The C API-only call-back functions are all thread safe:</span></span>
  
- <span data-ttu-id="b9144-177">**xlCoerce** (sauf en cas d��chec de for�age de type de références de cellule non calcul�e)</span><span class="sxs-lookup"><span data-stu-id="b9144-177">**xlCoerce** (except although coercion of uncalculated cell references fails)</span></span> 
    
- <span data-ttu-id="b9144-178">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="b9144-178">**xlFree**</span></span>
    
- <span data-ttu-id="b9144-179">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="b9144-179">**xlStack**</span></span>
    
- <span data-ttu-id="b9144-180">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="b9144-180">**xlSheetId**</span></span>
    
- <span data-ttu-id="b9144-181">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="b9144-181">**xlSheetNm**</span></span>
    
- <span data-ttu-id="b9144-182">**xlAbort** (sauf lorsqu�elle est utilis�e pour effacer une condition d�arr�t)</span><span class="sxs-lookup"><span data-stu-id="b9144-182">**xlAbort** (except when used to clear a break condition)</span></span> 
    
- <span data-ttu-id="b9144-183">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="b9144-183">**xlGetInst**</span></span>
    
- <span data-ttu-id="b9144-184">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="b9144-184">**xlGetHwnd**</span></span>
    
- <span data-ttu-id="b9144-185">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="b9144-185">**xlGetBinaryName**</span></span>
    
- <span data-ttu-id="b9144-186">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="b9144-186">**xlDefineBinaryName**</span></span>
    
<span data-ttu-id="b9144-187">La seule exception est la fonction **xlSet**, qui n�est en aucun cas un �quivalent de la commande, et par cons�quent ne peut pas �tre appel�e � partir de n�importe quelle fonction de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="b9144-187">The one exception is the **xlSet** function, which is, in any case, a command-equivalent and so cannot be called from any worksheet function.</span></span> 
  
<span data-ttu-id="b9144-p107">Une fonction de feuille de calcul�XLL peut �tre enregistr�e aupr�s d�Excel en tant que thread-safe. Cela indique � Excel que la fonction peut �tre appel�e en toute s�curit� et simultan�ment sur plusieurs threads, mais vous devez tout de m�me vous assurer que c�est bien le cas. Vous pouvez �ventuellement d�stabiliser Excel si une fonction enregistr�e comme thread-safe a un comportement non s�curis� par la suite.</span><span class="sxs-lookup"><span data-stu-id="b9144-p107">An XLL worksheet function can be registered with Excel as thread safe. This tells Excel that the function can be called safely and simultaneously on multiple threads, although you must make sure this is really the case. You can possibly destabilize Excel if a function registered as thread safe then behaves unsafely.</span></span>
  
## <a name="registering-xll-functions-as-thread-safe"></a><span data-ttu-id="b9144-191">Enregistrement de fonctions XLL comme thread-safe</span><span class="sxs-lookup"><span data-stu-id="b9144-191">Registering XLL functions as thread safe</span></span>
<span data-ttu-id="b9144-192"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="b9144-192"><a name="xl2007xllsdk_threadsafe"> </a></span></span>

<span data-ttu-id="b9144-193">Les r�gles qu�un d�veloppeur doit respecter lors de l��criture de fonctions thread-safe sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b9144-193">The rules that a developer must obey when writing thread-safe functions are as follows:</span></span>
  
- <span data-ttu-id="b9144-194">n�appelez pas de ressources dans d�autres DLL qui ne sont peut-�tre pas thread-safe�;</span><span class="sxs-lookup"><span data-stu-id="b9144-194">Do not call resources in other DLLs that may not be thread safe.</span></span>
    
- <span data-ttu-id="b9144-195">n��mettez pas d�appels non s�curis�s via l�API C ou COM�;</span><span class="sxs-lookup"><span data-stu-id="b9144-195">Do not make any thread-unsafe calls via the C API or COM.</span></span>
    
- <span data-ttu-id="b9144-196">prot�gez les ressources qui peuvent �tre utilis�es simultan�ment par plusieurs threads � l�aide des sections critiques�;</span><span class="sxs-lookup"><span data-stu-id="b9144-196">Protect resources that could be used simultaneously by more than one thread using critical sections.</span></span>
    
- <span data-ttu-id="b9144-197">utilisez la m�moire locale de thread pour le stockage propre au thread et remplacez les variables statiques dans les fonctions par des variables locales de thread.</span><span class="sxs-lookup"><span data-stu-id="b9144-197">Use thread-local memory for thread-specific storage, and replace static variables within functions with thread-local variables.</span></span>
    
<span data-ttu-id="b9144-198">Excel impose une restriction suppl�mentaire : les fonctions thread-safe ne peuvent pas �tre enregistr�es comme des �quivalents de feuilles macro, et par cons�quent ne peuvent pas appeler de fonctions d�informations XLM ou obtenir les valeurs des cellules non recalcul�es.</span><span class="sxs-lookup"><span data-stu-id="b9144-198">Excel imposes an additional restriction: thread-safe functions cannot be registered as macro-sheet equivalents, and therefore cannot call XLM information functions or get the values of un-recalculated cells.</span></span>
  
## <a name="memory-contention"></a><span data-ttu-id="b9144-199">Contention de mémoire</span><span class="sxs-lookup"><span data-stu-id="b9144-199">Memory contention</span></span>
<span data-ttu-id="b9144-200"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="b9144-200"><a name="xl2007xllsdk_threadsafe"> </a></span></span>

<span data-ttu-id="b9144-201">Les systémes multithread doivent traiter des probl�mes fondamentaux :</span><span class="sxs-lookup"><span data-stu-id="b9144-201">Multithreaded systems must address two fundamental issues:</span></span>
  
- <span data-ttu-id="b9144-202">comment prot�ger la m�moire utilis�e en lecture et en �criture � l�aide de plusieurs threads�;</span><span class="sxs-lookup"><span data-stu-id="b9144-202">How to protect memory that must be read from, or written to, by more than one thread.</span></span>
    
- <span data-ttu-id="b9144-203">comment cr�er et acc�der � une m�moire associ�e et propre au thread en cours d�ex�cution.</span><span class="sxs-lookup"><span data-stu-id="b9144-203">How to create and access memory that is associated with, and so private to, the executing thread.</span></span>
    
<span data-ttu-id="b9144-p108">Le systéme d�exploitation Windows et le kit de d�veloppement logiciel (SDK) Windows fournissent des outils pour ces deux �l�ments : des sections critiques et l�API de stockage local de thread (TLS), respectivement. Pour plus d�informations, voir [Gestion de la m�moire dans Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="b9144-p108">The Windows operating system and Windows Software Development Kit (SDK) provide tools for both of these: critical sections and the thread-local storage (TLS) API respectively. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="b9144-p109">Le premier probl�me peut se produire, par exemple, lorsque deux fonctions de feuille de calcul (ou deux instances de la m�me fonction en cours d�ex�cution simultan�ment) doivent acc�der � ou modifier une variable globale dans un projet DLL. N�oubliez pas qu�une telle variable globale peut �tre masqu�e dans une instance d�objet de classe accessible globalement.</span><span class="sxs-lookup"><span data-stu-id="b9144-p109">The first issue can arise, for example, when two worksheet functions (or two simultaneously running instances of the same function) need to access or modify a global variable in a DLL project. Remember that such a global variable might be hidden in a globally accessible instance of a class object.</span></span>
  
<span data-ttu-id="b9144-p110">Le deuxi�me probl�me peut se produire, par exemple, lorsqu�une fonction de feuille de calcul d�clare une variable ou un objet statique dans le code du corps de fonction. Le compilateur C/C++ cr�e uniquement une copie unique utilis�e par tous les threads. Cela signifie qu�une instance de la fonction peut modifier la valeur, tandis qu�une autre instance sur un autre thread peut supposer que la valeur est celle pr�c�demment d�finie.</span><span class="sxs-lookup"><span data-stu-id="b9144-p110">The second issue can arise, for example, when a worksheet function declares a static variable or object within the function body code. The C/C++ compiler only creates a single copy that all threads use. This means one instance of the function could change the value, while another on a different thread might be assuming the value is what it previously set.</span></span>
  
## <a name="example-applications-of-mtr"></a><span data-ttu-id="b9144-211">Exemple d’applications de recalcul multithread</span><span class="sxs-lookup"><span data-stu-id="b9144-211">Example applications of MTR</span></span>
<span data-ttu-id="b9144-212"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="b9144-212"><a name="xl2007xllsdk_threadsafe"> </a></span></span>

<span data-ttu-id="b9144-p111">Tout �l�ment�XLL qui exporte des fonctions de feuille de calcul peut tirer parti du recalcul multithread (MTR) dans Excel, � condition que ces fonctions n�aient pas � effectuer d�actions non thread-safe. Cela permet � Excel de recalculer les classeurs qui d�pendent d�eux-m�mes aussi rapidement que possible. Il s�agit donc d�un �l�ment souhaitable, quelle que soit l�application.</span><span class="sxs-lookup"><span data-stu-id="b9144-p111">Any XLL that exports worksheet functions can take advantage of multithreaded recalculation (MTR) in Excel provided that those functions do not need to perform thread-unsafe actions. This enables Excel to recalculate workbooks that depend on them as quickly as possible and is therefore desirable whatever the application.</span></span>
  
<span data-ttu-id="b9144-p112">Plus pr�cis�ment, le recalcul multithread a un impact consid�rable sur la dur�e de recalcul des classeurs qui appellent des fonctions d�finies par l�utilisateur, qui appellent elles-m�mes des processus externes pour obtenir le r�sultat souhait�. En particulier, envisagez une fonction d�finie par l�utilisateur qui appelle un serveur distant pouvant traiter plusieurs demandes simultan�ment, et un classeur contenant un grand nombre d�appels vers cette fonction. Si le recalcul du classeur est monothread, chaque appel � la fonction d�finie par l�utilisateur, et donc au serveur distant, doit �tre termin� avant de pouvoir r�aliser le suivant. De ce fait, le serveur perd sa capacit� � traiter plusieurs appels � la fois. Si le recalcul du classeur est multithread, Excel peut effectuer plusieurs appels � la fois ou dans un court laps de temps.</span><span class="sxs-lookup"><span data-stu-id="b9144-p112">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result. In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function. If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made. This wastes the server's ability to process many calls at once. If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span></span>
  
<span data-ttu-id="b9144-p113">Si Excel est configur� pour utiliser le m�me nombre de threads que le serveur (appel� N), et que la topologie de l�arborescence des d�pendances du classeur le permet, la dur�e de recalcul totale peut �tre r�duite � une valeur proche de 1/N de la dur�e de calcul monothread. Cette action peut s�av�rer efficace, m�me lorsque l�ordinateur client (sur lequel le classeur est en cours d�ex�cution) n�a qu�un processeur, en particulier lorsque le temps n�cessaire pour effectuer l�appel vers le serveur est court par rapport � la dur�e n�cessaire au serveur pour �mettre l�appel.</span><span class="sxs-lookup"><span data-stu-id="b9144-p113">If Excel is configured to use the same number of threads as the server—call it N—and the topology of the dependency tree of the workbook permits it, the total recalculation time could be reduced to something approaching 1/N of the single-threaded calculation time. This may be true even where the client computer (on which the workbook is running) only has one processor, especially where the time taken to make the call to the server is small relative to the time it takes the server to process the call.</span></span> 
  
<span data-ttu-id="b9144-p114">Il existe une surcharge du systéme d�exploitation pour chaque thread suppl�mentaire. Par cons�quent, un peu de pratique peut �tre requise pour un classeur donn� et un ordinateur serveur et client donn� pour trouver le nombre optimal de threads qu�Excel doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="b9144-p114">There is operating system overhead for each additional thread. Therefore some experimentation might be required for a given workbook and a given server and client computer to find the optimum number of threads Excel should be told to use.</span></span> 
  
<span data-ttu-id="b9144-p115">Par exemple, imaginez un ordinateur monoprocesseur ex�cutant Excel et un classeur contenant 1�000�cellules. Il appelle une fonction d�finie par l�utilisateur, qui � son tour appelle un ou plusieurs serveurs � distance. Supposons que les 1�000�cellules ne d�pendent pas les unes des autres, afin que Microsoft�Excel n�ait pas � attendre la fin d�un appel avant d�effectuer l�appel suivant. (Une relaxation de cette contrainte est possible sans influer cet exemple). Si les serveurs peuvent traiter 100�demandes simultan�ment, et qu�Excel est configur� pour utiliser 100�threads, le temps d�ex�cution peut �tre r�duit � une valeur aussi faible que 1/100e de la valeur lorsqu�un seul thread est utilis�. La surcharge qui est associ�e � Excel allouant des appels � chaque thread et au systéme d�exploitation g�rant 100�threads signifie que, dans la pratique, la r�duction ne sera pas vraiment id�ale. Il existe �galement une hypoth�se implicite selon laquelle le serveur est �volutif, et que le fait de lui demander de traiter 100�t�ches simultan�ment n�aura pas d�impact consid�rable sur les dur�es individuelles de traitement des t�ches.</span><span class="sxs-lookup"><span data-stu-id="b9144-p115">For example, consider a single-processor computer that is running Excel and a workbook that contains 1,000 cells. It calls a UDF, which in turn calls one or more remote servers. Assume that the 1,000 cells do not depend upon each other, so that Excel does not have to wait for one call to complete before calling the next. (Some relaxation of this constraint is possible without affecting this example.) If the servers can process 100 requests simultaneously, and Excel is configured to use 100 threads, the execution time can be reduced to as little as 1/100th of that where only one thread is used. The overhead that is associated with Excel allocating calls to each thread and the operating system managing 100 threads means that, in practice, the reduction will not be quite this great. There is also an implicit assumption here that the server scales well, and asking it to process 100 tasks concurrently will not affect individual task completion times significantly.</span></span>
  
<span data-ttu-id="b9144-230">Une application pratique dans laquelle cette technique peut repr�senter des avantages importants est celle des m�thodes Monte�Carlo, ainsi que d�autres t�ches intensives num�riques qui peuvent �tre divis�es en sous-t�ches moins volumineuses pouvant �tre confi�es aux serveurs.</span><span class="sxs-lookup"><span data-stu-id="b9144-230">One practical application in which this technique can have an important benefit is that of Monte-Carlo methods, as well as other numerically intensive tasks that can be split into smaller sub-tasks that can be farmed out to servers.</span></span>
  
## <a name="excel-services-considerations"></a><span data-ttu-id="b9144-231">Remarques sur Excel Services</span><span class="sxs-lookup"><span data-stu-id="b9144-231">Excel Services considerations</span></span>
<span data-ttu-id="b9144-232"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="b9144-232"><a name="xl2007xllsdk_threadsafe"> </a></span></span>

<span data-ttu-id="b9144-p116">Les services Excel prennent en charge le chargement, le calcul et le rendu des feuilles de calcul Excel sur un serveur. Les utilisateurs peuvent ensuite acc�der aux feuilles de calcul et interagir avec celles-ci � l�aide d�outils de navigateur standard.</span><span class="sxs-lookup"><span data-stu-id="b9144-p116">Excel Services supports the loading, calculating, and rendering of Excel spreadsheets on a server. Users can then access and interact with the spreadsheets by using standard browser tools.</span></span>
  
<span data-ttu-id="b9144-p117">Les fonctions d�finies par l�utilisateur des services Excel sont cr��es � l�aide du code manag� Microsoft�.NET�Framework et sont disponibles via un assembly�.NET. Les XLL ne sont pas pris en charge par les services Excel. Une ressource de fonction d�finie par l�utilisateur de serveur de code manag� peut appeler un XLL afin qu�il acc�de � ses fonctionnalit�s, de sorte que l�utilisateur peut avoir la m�me fonctionnalit� avec un classeur charg� sur le serveur qu�avec un classeur charg� sur le client.</span><span class="sxs-lookup"><span data-stu-id="b9144-p117">Excel Services UDFs are created using Microsoft .NET Framework managed code and made available though a .NET assembly. XLLs are not supported by Excel Services. A managed code server UDF resource can call into an XLL to access its functionality, so that the user can have the same functionality with a server-loaded workbook as with a client-loaded workbook.</span></span>
  
<span data-ttu-id="b9144-p118">Pour que les fonctions d�un XLL soient disponibles de cette fa�on, elles doivent �tre encapsul�es dans un assembly�.NET qui convertit les arguments et renvoie des valeurs � partir des types de donn�es natives vers des types de donn�es manag�es�.NET�Framework, et qui appelle les fonctions�XLL. Le wrapper�.NET exporte un seul serveur de fonction d�finie par l�utilisateur pour chaque fonction XLL � laquelle l�utilisateur acc�de. Une autre condition requise est que toutes les fonctions XLL appel�es de cette fa�on doivent �tre thread-safe. �tant donn� que les fonctions XLL ne sont pas enregistr�es de la m�me mani�re qu�avec le client Excel, le serveur et le wrapper�.NET n�ont aucun moyen de v�rifier qu�elles sont thread-safe. Il incombe au d�veloppeur XLL de s�en assurer.</span><span class="sxs-lookup"><span data-stu-id="b9144-p118">To make an XLL's functions available in this way, they must therefore be wrapped in a .NET assembly that converts arguments and return values from the native data types to the .NET Framework managed data types, and that calls the XLL functions. The .NET wrapper would export one server UDF for each XLL function being accessed. An additional requirement is that any XLL functions called in this way must be thread safe. Because the XLL functions are not registered in the way that they are with client Excel, the server and the .NET wrapper have no way of enforcing that they are thread safe. It is the responsibility of the XLL developer to ensure this.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9144-243">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9144-243">See also</span></span>

- [<span data-ttu-id="b9144-244">Recalcul Excel</span><span class="sxs-lookup"><span data-stu-id="b9144-244">Excel Recalculation</span></span>](excel-recalculation.md)  
- [<span data-ttu-id="b9144-245">Gestion de la mémoire dans Excel</span><span class="sxs-lookup"><span data-stu-id="b9144-245">Memory Management in Excel</span></span>](memory-management-in-excel.md) 
- [<span data-ttu-id="b9144-246">Accés au code XLL dans Excel</span><span class="sxs-lookup"><span data-stu-id="b9144-246">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="b9144-247">Concepts de programmation Excel</span><span class="sxs-lookup"><span data-stu-id="b9144-247">Excel Programming Concepts</span></span>](excel-programming-concepts.md)  
- [<span data-ttu-id="b9144-248">Référence des fonctions XLL SDK API Excel 2013</span><span class="sxs-lookup"><span data-stu-id="b9144-248">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

