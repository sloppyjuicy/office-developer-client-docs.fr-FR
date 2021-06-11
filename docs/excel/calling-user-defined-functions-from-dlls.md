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
# <a name="calling-user-defined-functions-from-dlls"></a>Appel des fonctions définies par l’utilisateur à partir de fichiers DLL

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Appeler des fonctions définies par l’utilisateur à partir d’une feuille de calcul est aussi simple qu’appeler des fonctions intégrées : vous entrez la fonction via une formule de cellule. Toutefois, à partir de l’API C, il n’existe pas de codes de fonction prédéfin définis à utiliser avec les call-backs. Pour vous permettre d’appeler des fonctions UDF, l’API C exporte une fonction XLL uniquement, la [fonction xlUDF.](xludf.md) Le premier argument de la fonction est le nom de la fonction en tant que chaîne, et les arguments suivants sont ceux que l’UDF attend normalement. 
  
Vous pouvez obtenir la liste des commandes et fonctions de la XLL actuellement inscrites à l’aide de la fonction **xlfGetWorkspace** avec l’argument 44. Cela renvoie un tableau de trois colonnes où les colonnes représentent les points suivants : 
  
- Chemin d’accès complet et nom du XLL
    
- Nom de l’UDF ou de la commande exportée à partir de la XLL
    
- Chaîne de code de retour et d’argument
    
> [!NOTE]
> Le nom exporté à partir du XLL peut ne pas être identique au nom enregistré par lequel Excel connaît la UDF ou la commande. 
  
À compter de Excel 2007, les fonctions de la boîte à outils Analysis Toolpak (ATP) sont entièrement intégrées et l’API C possède ses propres éumérations pour des fonctions telles que PRICE, **xlfPrice**. Dans les versions antérieures, vous deviez utiliser **xlUDF** pour appeler ces fonctions. Si votre add-in doit fonctionner avec Excel 2003 et Excel 2007 ou versions ultérieures et qu’il utilise ces fonctions, vous devez détecter la version actuelle et appeler la fonction de la manière appropriée. 
  
## <a name="examples"></a>Exemples

L’exemple suivant montre la fonction **xlUDF** utilisée pour appeler la fonction ATP **PRICE** lorsque la version d’exécution de Excel est 2003 ou une version antérieure. Pour plus d’informations sur la définition d’une variable de version globale, telle que **gExcelVersion12plus** dans cet exemple, voir [Compatibilité ascendante.](backward-compatibility.md)
  
> [!NOTE]
> Cet exemple utilise les fonctions **Framework TempNum**, **TempStrConst** pour configurer les arguments et Excel l’API C. 
  
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

Lorsque vous appelez une fonction XLL qui renvoie une valeur en modifiant un argument en place, la fonction **xlUDF** renvoie toujours la valeur via l’adresse du résultat **XLOPER/XLOPER12**. En d’autres termes, le résultat est renvoyé comme s’il s’agit d’une instruction de retour normale. La **xlOPER/XLOPER12** qui correspond à l’argument utilisé pour la valeur de retour n’est pasmodifiée. Par exemple, prenons les deux UDF suivantes. 
  
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

Lorsque **UDF \_ 2** appelle **UDF \_ 1,** la valeur de **pxArg** reste inchangée après l’appel à **Excel12** et la valeur renvoyée par **UDF_1** est contenue dans **xRetVal**.
  
Lorsque vous faites un grand nombre d’appels à une fonction UDF de cette façon, vous pouvez d’abord évaluer le nom de la fonction à l’aide de la fonction [xlfEvaluate](xlfevaluate.md). Le numéro résultant, qui est identique à l’ID d’inscription renvoyé par la fonction **xlfRegister,** peut être passé à la place du nom de la fonction comme premier argument de la fonction **xlUDF.** Cela permet Excel rechercher et appeler la fonction plus rapidement que si elle doit rechercher le nom de la fonction à chaque fois. 
  
## <a name="see-also"></a>Voir aussi

- [Autorisation des interruptions utilisateur lors des opérations très longues](permitting-user-breaks-in-lengthy-operations.md)
- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013](getting-started-with-the-excel-xll-sdk.md)

