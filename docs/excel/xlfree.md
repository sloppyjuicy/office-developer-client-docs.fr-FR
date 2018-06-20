---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- fonction xlFree [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782230"
---
# <a name="xlfree"></a>xlFree

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour libérer de la mémoire de ressources alloués par Microsoft Excel lors de la création du retour valeur **XLOPER**/ **XLOPER12** dans un appel à [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)ou [Excel12v](excel4v-excel12v.md). La fonction **xlFree** libère la mémoire auxiliaire et réinitialise le pointeur de la **valeur null** , mais ne supprime pas les autres parties de la **XLOPER**/ **XLOPER12**.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Paramètres

 _px_1,..., px_n_
  
Un ou plusieurs **XLOPER**/ s**XLOPER12**à libérer. Dans les versions Excel jusqu'à 2003, le nombre maximal de pointeurs qui peut être passé est 30. À compter d’Excel 2007, il est augmentée à 255.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

Cette fonction ne retourne pas une valeur.
  
## <a name="remarks"></a>Remarques

Vous devez libérer chaque **XLOPER** que vous obtenez en tant qu’une valeur de retour **Excel4** ou **Excel4v** et chaque **XLOPER12** que vous obtenez comme valeur de retour **d’Excel12** ou **Excel12v** s’il s’agit des types suivants : xltypeStr ** **, **xltypeMulti**ou **xltypeRef**. Il est recommandé d’autres types de même si elles n’utilisent pas la mémoire auxiliaire, dans la mesure où les obtenue depuis **Excel4** ou **Excel12**.
  
Lorsque vous retournez à Excel un pointeur vers un **XLOPER**/ **XLOPER12** qui contient toujours mémoire allouée Excel à libérer, vous devez définir la **xlbitXLFree** la mémoire pour les versions d’Excel. 
  
## <a name="example"></a>Exemple

Cet exemple appelle **obtenir. WORKSPACE(1)** pour renvoyer la plate-forme les Excel est en cours d’exécution sous forme de chaîne. Le code copie ce retourné de chaîne dans une mémoire tampon pour une utilisation ultérieure. Le code place la mémoire tampon dans le **XLOPER12** pour une utilisation ultérieure avec la fonction Excel. Enfin, le code affiche la chaîne dans un message d’alerte. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Voir aussi

- [Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

