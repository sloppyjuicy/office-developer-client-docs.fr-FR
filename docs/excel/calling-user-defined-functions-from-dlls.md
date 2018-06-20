---
title: Appel de fonctions définies par l’utilisateur à partir de DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- UDF [excel 2007], appel à partir de DLL, fonctions définies par l’utilisateur [Excel 2007], appel à partir de DLL, DLL [Excel 2007], l’appel des UDF
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4e893cf1e54489610315dd5c5d57bd78c3c936d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782022"
---
# <a name="calling-user-defined-functions-from-dlls"></a>Appel de fonctions définies par l’utilisateur à partir de DLL

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
L’appel de fonctions définies par l’utilisateur (UDF) à partir d’une feuille de calcul est aussi simple que l’appel de fonctions intégrées : vous permet d’entrer la fonction via une formule de cellule. Toutefois, à partir de l’API C, il n’existe aucun code fonction prédéfinie à utiliser avec les rappels. Pour vous permettre d’appeler des UDF, l’API C exporte une fonction XLL uniquement, la fonction [xlUDF](xludf.md) . Premier argument de la fonction est le nom de la fonction sous forme de chaîne, et les arguments suivants sont ceux qui l’UDF attendriez normalement. 
  
Vous pouvez obtenir une liste des commandes actuellement XLL complément inscrite à l’aide de la fonction **xlfGetWorkspace** avec l’argument 44. Cet exemple renvoie un tableau de trois colonnes où les colonnes représentent les éléments suivants : 
  
- Le chemin d’accès complet et le nom de la ressource XLL
    
- Le nom de la commande comme exporté à partir de la ressource XLL ou un fichier UDF
    
- La chaîne de code de retour et l’argument
    
> [!NOTE]
> Le nom comme exporté à partir de la ressource XLL ne peut pas être le même que le nom enregistré par lequel Excel connaît l’UDF ou la commande. 
  
À compter d’Excel 2007, les fonctions de l’utilitaire d’analyse (DAV) sont entièrement intégrées, et l’API C a son propre énumérations de fonctions telles que les prix, **xlfPrice**. Dans les versions précédentes, vous deviez utiliser **xlUDF** pour appeler ces fonctions. Si votre complément doit travailler avec Excel 2003 et Excel 2007 ou versions ultérieures, et il utilise ces fonctions, vous devez détecter la version actuelle et appelez la fonction de la manière appropriée. 
  
## <a name="examples"></a>Exemples

L’exemple suivant montre la fonction **xlUDF** utilisée pour appeler **la fonction DAV** lorsque la version d’Excel en cours d’exécution est 2003 ou version antérieure. Pour plus d’informations sur la définition d’une variable globale de version, tel que **gExcelVersion12plus** dans cet exemple, voir [Compatibilité descendante](backward-compatibility.md).
  
> [!NOTE]
> Cet exemple utilise les fonctions Framework **TempNum**, **TempStrConst** pour définir des arguments et Excel pour appeler l’API C. 
  
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

Lorsque vous appelez une fonction XLL qui renvoie une valeur en modifiant un argument en place, la fonction **xlUDF** renvoie toujours la valeur via l’adresse du résultat **XLOPER/XLOPER12**. En d’autres termes, le résultat est renvoyé comme si via une instruction return normale. Le **XLOPER/XLOPER12** qui correspond à l’argument est utilisé pour la valeur de retour est non modifié. Prenons l’exemple suivants deux fonctions UDF. 
  
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

Lorsque **UDF\_2** appels **UDF\_1**, la valeur de **pxArg** est inchangée après l’appel à **Excel12**et la valeur renvoyée par **UDF_1** est contenue dans **xRetVal**.
  
Lorsque vous effectuez un grand nombre d’appels vers un fichier UDF de cette manière, vous pouvez évaluer tout d’abord le nom de la fonction à l’aide de la [fonction xlfEvaluate](xlfevaluate.md). Le numéro qui en résulte, qui est la même que l’ID de l’enregistrement qui est renvoyé par la fonction **xlfRegister** , peut être passé à la place du nom de la fonction comme premier argument à la fonction **xlUDF** . Cela permet à Microsoft Excel pour rechercher et appeler la fonction plus rapidement que si elle doit rechercher le nom de la fonction de chaque fois. 
  
## <a name="see-also"></a>Voir aussi

- [Autorisation utilisateur sauts dans les opérations de longue durée](permitting-user-breaks-in-lengthy-operations.md)
- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)

