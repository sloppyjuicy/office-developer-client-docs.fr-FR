---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- fonction temperr [excel 2007], fonction TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782189"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** contenant une erreur de feuille de calcul Microsoft Excel. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Paramètres

 _message d’erreur_
  
Le code d’erreur de votre choix, ou son équivalent numérique littérale, comme indiqué dans le tableau suivant.
  
|**Erreur**|**Code d’erreur défini dans XLCALL. H**|**Équivalent décimal**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7  <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15  <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>Valeur renvoy�e

Renvoie une **xltypeBool** contenant le code d’erreur passé. 
  
## <a name="example"></a>Exemple

Cet exemple utilise la fonction **TempErr12** pour renvoyer un #VALUE ! erreur Excel. 
  
> [!NOTE]
> La fonction de bibliothèque Framework **TempErr12** alloue de la mémoire d’un tampon interne, qui est libéré normalement lorsque la fonction de la structure **Excel12f** est appelée. Si cet exemple de fonction est appelé à plusieurs reprises sans **Excel12f** appelée, une fuite de mémoire se produit. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>Voir aussi



[Fonctions de la bibliothèque Framework](functions-in-the-framework-library.md)

