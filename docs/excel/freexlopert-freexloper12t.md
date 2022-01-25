---
title: FreeXLOperT/FreeXLOper12T
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FreeXLOper12T
- FreeXLOperT
keywords:
- fonction freexlopert [excel 2007],Fonction FreeXLOper12T [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 8fb3fdfd-8a43-4c50-82ff-e701fed3d83f
ms.openlocfilehash: 1deed00456d321665a154e854e2af6b86ba2c60f
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199025"
---
# <a name="freexlopertfreexloper12t"></a>FreeXLOperT/FreeXLOper12T

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction Framework qui libère la mémoire associée à **une structure** /  **XLOPER XLOPER12**. La fonction suppose que la mémoire a été allouée avec des appels à malloc dans la DLL. Si la mémoire a été allouée par Microsoft Excel ou d’une autre manière ou par un autre processus, cette fonction ne doit pas être utilisée pour libérer la mémoire. Utilisez [xlFree pour](xlfree.md) libérer de la mémoire allouée par Excel **xlOPER** /  **XLOPER12** s. 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Paramètres

 _pxloper_ (**LPXLOPER**)
  
 _pxloper12_ (**LPXLOPER12**)
  
Pointeur vers **la XLOPER** /  **XLOPER12** à libérer. 
  
## <a name="example"></a>Exemple

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
void FreeXLOper12T(LPXLOPER12 pxloper12)
{
   DWORD xltype;
   int cxloper12;
   LPXLOPER12 pxloper12Free;
   xltype = pxloper12->xltype;
   switch (xltype)
   {
   case xltypeStr:
      if (pxloper12->val.str != NULL)
         free(pxloper12->val.str);
      break;
   case xltypeRef:
      if (pxloper12->val.mref.lpmref != NULL)
         free(pxloper12->val.mref.lpmref);
      break;
   case xltypeMulti:
      cxloper12 = pxloper12->val.array.rows * pxloper12->val.array.columns;
      if (pxloper12->val.array.lparray)
      {
         pxloper12Free = pxloper12->val.array.lparray;
         while (cxloper12 > 0)
         {
            FreeXLOper12T(pxloper12Free);
            pxloper12Free++;
            cxloper12--;
         }
         free(pxloper12->val.array.lparray);
      }
      break;
   case xltypeBigData:
      if (pxloper12->val.bigdata.h.lpbData != NULL)
         free(pxloper12->val.bigdata.h.lpbData);
      break;
   }
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

