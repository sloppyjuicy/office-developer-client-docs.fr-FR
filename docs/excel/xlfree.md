---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- fonction xlFree [Excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: de1c75ad65acacd44644e9bfb111b30abd0a578e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310219"
---
# <a name="xlfree"></a>xlFree

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour libérer de la mémoire les ressources allouées par Microsoft Excel lors de la création de la valeur de retour **XLOPER**/ **XLOPER12** dans un appel à [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)ou [Excel12v](excel4v-excel12v.md). La **fonction xlFree** libère la mémoire auxiliaire et réinitialise le pointeur sur **null** , mais ne détruit pas les autres parties de la ****/ **** définition d'éléments de la structure de la définition.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Paramètres

 _px_1,..., px_n_
  
Un ou plusieurs objets **XLOPER**/ **XLOPER12**doivent être libérés. Dans les versions d'Excel allant jusqu'à 2003, le nombre maximal de pointeurs pouvant être transmis est de 30. À partir d'Excel 2007, cette progression est augmentée à 255.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Cette fonction ne renvoie pas de valeur.
  
## <a name="remarks"></a>Remarques

Vous devez libérer tous les éléments **XLOPER** que vous obtenez sous forme de valeur de retour de **Excel4** ou **Excel4v** et chaque **XLOPER12** que vous obtenez sous forme de valeur de retour de **Excel12** ou **Excel12v** s'il s'agit de l'un des types suivants: **xltypeStr **, **XltypeMulti**ou **xltypeRef**. Il est toujours sûr de ne pas utiliser d'autres types même s'ils n'utilisent pas de mémoire auxiliaire, à condition que vous les obteniez de **Excel4** ou **Excel12**.
  
Où vous retournez dans Excel un pointeur vers une expression **XLOPER**/ **** qui contient toujours de la mémoire allouée à Excel à libérer, vous devez définir la **xlbitXLFree** pour vous assurer que Excel libère la mémoire. 
  
## <a name="example"></a>Exemple

Cet exemple appelle **Get. WORKSPACE (1)** pour renvoyer la plateforme sur laquelle Excel est en cours d'exécution en tant que chaîne. Le code copie cette chaîne renvoyée dans un buffer pour une utilisation ultérieure. Le code place la mémoire tampon dans le **XLOPER12** pour une utilisation ultérieure avec la fonction Excel. Enfin, le code affiche la chaîne dans un message d'alerte. 
  
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

- [Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

