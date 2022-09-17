---
title: Appel des fonctions définies par l’utilisateur à partir de fichiers DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], appels à partir de dlls, fonctions définies par l’utilisateur [Excel 2007], appels à partir de DLL, DLL [Excel 2007], appels de fonctions définies par l’utilisateur
ms.localizationpriority: medium
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
ms.openlocfilehash: 37f3c359dc0303e20968f44ca330f2a7f7ae6228
ms.sourcegitcommit: 9d63c4fab7bca6b2a14f9883334abbc6c490d711
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2022
ms.locfileid: "67796009"
---
# <a name="calling-user-defined-functions-from-dlls"></a>Appel des fonctions définies par l’utilisateur à partir de fichiers DLL

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
L’appel de fonctions définies par l’utilisateur (UDF) à partir d’une feuille de calcul est aussi simple que l’appel de fonctions intégrées : vous entrez la fonction via une formule de cellule. Toutefois, à partir de l’API C, il n’existe aucun code de fonction prédéfini à utiliser avec les rappels. Pour vous permettre d’appeler des fonctions définies par l’utilisateur, l’API C exporte une fonction XLL uniquement, la fonction [xlUDF ](xludf.md) . Le premier argument de la fonction est le nom de la fonction sous forme de chaîne, et les arguments suivants sont ceux que l’UDF attend normalement. 
  
Vous pouvez obtenir la liste des fonctions et commandes de complément XLL actuellement inscrites à l’aide de la fonction **xlfGetWorkspace** avec l’argument 44. Cela retourne un tableau à trois colonnes où les colonnes représentent les éléments suivants : 
  
- Chemin d’accès complet et nom de la XLL
    
- Nom de la fonction UDF ou de la commande exportée à partir de la XLL
    
- Chaîne de code de retour et d’argument
    
> [!NOTE]
> Le nom tel qu’exporté à partir de la XLL peut ne pas être le même que le nom inscrit par lequel Excel connaît la fonction UDF ou la commande. 
  
À compter d’Excel 2007, les fonctions ATP (Analysis Toolpak) sont entièrement intégrées et l’API C a ses propres énumérations pour des fonctions telles que PRICE, **xlfPrice**. Dans les versions antérieures, vous deviez utiliser **xlUDF** pour appeler ces fonctions. Si votre complément doit fonctionner avec Excel 2003 et Excel 2007 ou versions ultérieures, et qu’il utilise ces fonctions, vous devez détecter la version actuelle et appeler la fonction de la manière appropriée. 
  
## <a name="examples"></a>Exemples

L’exemple suivant montre la fonction **xlUDF** utilisée pour appeler la fonction ATP **PRICE** lorsque la version en cours d’exécution d’Excel est 2003 ou antérieure. Pour plus d’informations sur le paramètre d’une variable de version globale, telle que **gExcelVersion12plus** dans cet exemple, consultez [Compatibilité descendante](backward-compatibility.md).
  
> [!NOTE]
> Cet exemple utilise les fonctions Framework **TempNum**, **TempStrConst** pour configurer les arguments et Excel pour appeler l’API C. 
  
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


Lorsque vous appelez une fonction XLL qui retourne une valeur en modifiant un argument en place, la fonction **xlUDF** retourne toujours la valeur via l’adresse du **résultat XLOPER/XLOPER12**. En d’autres termes, le résultat est retourné comme s’il s’agit d’une instruction de retour normale. **XlOPER/XLOPER12** qui correspond à l’argument utilisé pour la valeur de retour n’est pas modifié. Par exemple, considérez les deux fonctions définies par l’utilisateur suivantes. 
  
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

Quand **UDF\_2** appelle **UDF\_1**, la valeur de **pxArg** est inchangée après l’appel à **Excel12**, et la valeur retournée par **UDF_1** est contenue dans **xRetVal**.
  
Lorsque vous effectuez un grand nombre d’appels à une fonction définie par l’utilisateur de cette façon, vous pouvez d’abord évaluer le nom de la fonction à l’aide de la [fonction xlfEvaluate](xlfevaluate.md). Le nombre résultant, qui est le même que l’ID d’inscription retourné par la fonction **xlfRegister** , peut être passé à la place du nom de la fonction comme premier argument à la fonction **xlUDF** . Cela permet à Excel de rechercher et d’appeler la fonction plus rapidement que si elle doit rechercher le nom de la fonction à chaque fois. 
  
## <a name="see-also"></a>Voir aussi

- [Autorisation des interruptions utilisateur lors des opérations très longues](permitting-user-breaks-in-lengthy-operations.md)
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)
