---
title: Appel des fonctions définies par l’utilisateur à partir de fichiers DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], calling from dlls,user-defined functions [Excel 2007], calling from DLLs,DLLs [Excel 2007], calling UDFs
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9e2ca3f4485fb41c5ab6a48f323b4c0093e747e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417944"
---
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="e1f85-104">Appel des fonctions définies par l’utilisateur à partir de fichiers DLL</span><span class="sxs-lookup"><span data-stu-id="e1f85-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="e1f85-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e1f85-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e1f85-106">Appeler des fonctions définies par l’utilisateur à partir d’une feuille de calcul est aussi simple qu’appeler des fonctions intégrées : vous entrez la fonction via une formule de cellule.</span><span class="sxs-lookup"><span data-stu-id="e1f85-106">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula.</span></span> <span data-ttu-id="e1f85-107">Toutefois, à partir de l’API C, il n’existe pas de codes de fonction prédéfin définis à utiliser avec les call-backs.</span><span class="sxs-lookup"><span data-stu-id="e1f85-107">However, from the C API, there are no pre-defined function codes to use with the call-backs.</span></span> <span data-ttu-id="e1f85-108">Pour vous permettre d’appeler des fonctions UDF, l’API C exporte une fonction XLL uniquement, la [fonction xlUDF.](xludf.md)</span><span class="sxs-lookup"><span data-stu-id="e1f85-108">To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function.</span></span> <span data-ttu-id="e1f85-109">Le premier argument de la fonction est le nom de la fonction en tant que chaîne, et les arguments suivants sont ceux que l’UDF attend normalement.</span><span class="sxs-lookup"><span data-stu-id="e1f85-109">The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="e1f85-110">Vous pouvez obtenir la liste des commandes et fonctions de la XLL actuellement inscrites à l’aide de la fonction **xlfGetWorkspace** avec l’argument 44.</span><span class="sxs-lookup"><span data-stu-id="e1f85-110">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44.</span></span> <span data-ttu-id="e1f85-111">Cela renvoie un tableau de trois colonnes où les colonnes représentent les points suivants :</span><span class="sxs-lookup"><span data-stu-id="e1f85-111">This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="e1f85-112">Chemin d’accès complet et nom du XLL</span><span class="sxs-lookup"><span data-stu-id="e1f85-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="e1f85-113">Nom de l’UDF ou de la commande exportée à partir du XLL</span><span class="sxs-lookup"><span data-stu-id="e1f85-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="e1f85-114">Chaîne de code de retour et d’argument</span><span class="sxs-lookup"><span data-stu-id="e1f85-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="e1f85-115">Le nom exporté à partir de la XLL peut ne pas être identique au nom enregistré par lequel Excel connaît l’UDF ou la commande.</span><span class="sxs-lookup"><span data-stu-id="e1f85-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="e1f85-116">À compter d’Excel 2007, les fonctions de la boîte à outils Analysis Toolpak (ATP) sont entièrement intégrées et l’API C possède ses propres éumérations pour des fonctions telles que PRICE, **xlfPrice**.</span><span class="sxs-lookup"><span data-stu-id="e1f85-116">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**.</span></span> <span data-ttu-id="e1f85-117">Dans les versions antérieures, vous deviez utiliser **xlUDF** pour appeler ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="e1f85-117">In earlier versions, you had to use **xlUDF** to call these functions.</span></span> <span data-ttu-id="e1f85-118">Si votre add-in doit fonctionner avec Excel 2003 et Excel 2007 ou versions ultérieures, et qu’il utilise ces fonctions, vous devez détecter la version actuelle et appeler la fonction de la manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="e1f85-118">If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="e1f85-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="e1f85-119">Examples</span></span>

<span data-ttu-id="e1f85-120">L’exemple suivant montre la **fonction xlUDF** utilisée pour appeler la fonction **ATP PRICE** lorsque la version en cours d’exécution d’Excel est 2003 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="e1f85-120">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier.</span></span> <span data-ttu-id="e1f85-121">Pour plus d’informations sur la définition d’une variable de version globale, telle que **gExcelVersion12plus** dans cet exemple, voir [Compatibilité ascendante.](backward-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="e1f85-121">For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="e1f85-122">Cet exemple utilise les fonctions Framework **TempNum**, **TempStrConst** pour configurer les arguments et Excel pour appeler l’API C.</span><span class="sxs-lookup"><span data-stu-id="e1f85-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
```C
LPXLOPER TempNum(double d);
LPXLOPER TempStrConst(const LPSTR lpstr);
int cdecl Excel(int xlfn, LPXLOPER pxResult, int count, ...);
double call_ATP_example(void)
{
  XLOPER xPrice;
  int xl_ret_val;
  if(gExcelVersion12plus) // Starting in Excel 2007
  {
    xl_ret_val = Excel(xlfPrice, &xPrice, 7,
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redemption value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  else // Excel 2003-
  {
    xl_ret_val = Excel(xlUDF, &xPrice, 8,
      TempStrConst("PRICE"),
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redepmtion value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  if(xl_ret_val != xlretSuccess || xPrice.xltype != xltypeNum)
  {
// Even though PRICE is not expected to return a string, there
// is no harm in freeing the XLOPER to be safe
    Excel(xlFree, 0, 1, &xPrice);
    return -1.0; // an error value
  }
  return xPrice.val.num;
}
```

<br/>

<span data-ttu-id="e1f85-123">Lorsque vous appelez une fonction XLL qui renvoie une valeur en modifiant un argument en place, la fonction **xlUDF** renvoie toujours la valeur via l’adresse du résultat **XLOPER/XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="e1f85-123">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**.</span></span> <span data-ttu-id="e1f85-124">En d’autres termes, le résultat est renvoyé comme s’il s’agit d’une instruction de retour normale.</span><span class="sxs-lookup"><span data-stu-id="e1f85-124">In other words, the result is returned as if through a normal return statement.</span></span> <span data-ttu-id="e1f85-125">La **xlOPER/XLOPER12** qui correspond à l’argument utilisé pour la valeur de retour n’est pasmodifiée.</span><span class="sxs-lookup"><span data-stu-id="e1f85-125">The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified.</span></span> <span data-ttu-id="e1f85-126">Par exemple, prenons les deux UDF suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1f85-126">For example, consider the following two UDFs.</span></span> 
  
```C
// Registered as "1E". Returns its argument incremented by 1.
void WINAPI UDF_1(double *pArg)
{
  *pArg += 1.0;
}
// Registered as "QQ". Returns its argument unmodified
// unless it is a number, in which case it increments it
// by calling UDF_1.
LPXLOPER12 WINAPI UDF_2(LPXLOPER12 pxArg)
{
  static XLOPER12 xRetVal; // Not thread-safe
  XLOPER12 xFn;
  xFn.xltype = xltypeStr;
  xFn.val.str = L"\005UDF_1";
  Excel12(xlUDF, &xRetVal, 2, &xFn, pxArg);
  xRetVal.xltype |= xlbitXLFree;
  return &xRetVal;
}
```

<span data-ttu-id="e1f85-127">Lorsque **UDF \_ 2** appelle **UDF \_ 1,** la valeur de **pxArg** reste inchangée après l’appel à **Excel12** et la valeur renvoyée par **UDF_1** est contenue dans **xRetVal**.</span><span class="sxs-lookup"><span data-stu-id="e1f85-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="e1f85-128">Lorsque vous faites un grand nombre d’appels à une fonction UDF de cette façon, vous pouvez d’abord évaluer le nom de la fonction à l’aide de la fonction [xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="e1f85-128">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="e1f85-129">Le nombre résultant, qui est identique à l’ID d’inscription renvoyé par la fonction **xlfRegister,** peut être passé à la place du nom de la fonction comme premier argument de la fonction **xlUDF.**</span><span class="sxs-lookup"><span data-stu-id="e1f85-129">The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function.</span></span> <span data-ttu-id="e1f85-130">Cela permet à Excel de rechercher et d’appeler la fonction plus rapidement que si elle doit rechercher le nom de la fonction à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="e1f85-130">This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1f85-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1f85-131">See also</span></span>

- [<span data-ttu-id="e1f85-132">Autorisation des interruptions utilisateur lors des opérations très longues</span><span class="sxs-lookup"><span data-stu-id="e1f85-132">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="e1f85-133">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="e1f85-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="e1f85-134">Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013</span><span class="sxs-lookup"><span data-stu-id="e1f85-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

