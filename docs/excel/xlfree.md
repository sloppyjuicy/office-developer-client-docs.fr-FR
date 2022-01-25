---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- fonction xlfree [excel 2007]
ms.localizationpriority: medium
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
ms.openlocfilehash: f33254cb1bba4e22e047f9daafd1d5945e395acb
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199555"
---
# <a name="xlfree"></a>xlFree

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilisé pour libérer des ressources mémoire allouées par Microsoft Excel lors de la création de la valeur de retour **XLOPER** XLOPER12 dans un appel à /   [Excel4,](excel4-excel12.md) [Excel4v,](excel4v-excel12v.md) [Excel12](excel4-excel12.md)ou [Excel12v](excel4v-excel12v.md). La **fonction xlFree** libère la mémoire auxiliaire et réinitialise le pointeur sur **NULL,** mais ne détruit pas les autres parties de la  /  **XLOPER XLOPER12**.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Paramètres

 _px_1, ..., px_n_
  
Une ou plusieurs **XLOPER** /  **XLOPER12** à libérer. Dans Excel versions jusqu’en 2003, le nombre maximal de pointeurs qui peuvent être transmis est de 30. À compter Excel 2007, ce nombre est passé à 255.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

Cette fonction ne retourne pas de valeur.
  
## <a name="remarks"></a>Remarques

Vous devez libérer chaque **XLOPER** que vous obtenez en tant que valeur de retour à partir **d’Excel4** ou **Excel4v** et de chaque **XLOPER12** que vous obtenez en tant que valeur de retour d’Excel12 ou **Excel12v** s’ils sont de l’un des types suivants : **xltypeStr,** **xltypeMulti** ou **xltypeRef**.  Il est toujours sûr de libérer d’autres types même s’ils n’utilisent pas de mémoire auxiliaire, tant que vous les avez obtenus à partir **d’Excel4** ou **Excel12**.
  
Lorsque vous revenir à Excel pointeur vers une **XLOPER** XLOPER12 qui contient encore une mémoire allouée Excel à libérer, vous devez définir /   **xlbitXLFree** pour vous assurer que Excel libère la mémoire. 
  
## <a name="example"></a>Exemple

Cet exemple appelle **GET. WORKSPACE(1)** pour renvoyer la plateforme sur laquelle Excel est en cours d’exécution sous forme de chaîne. Le code copie cette chaîne renvoyée dans une mémoire tampon pour une utilisation ultérieure. Le code place la mémoire tampon dans **xlOPER12** pour une utilisation ultérieure avec Excel fonction. Enfin, le code affiche la chaîne dans une zone d’alerte. 
  
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

