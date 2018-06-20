---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- fonction tempmissing [excel 2007], fonction TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782199"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="c455b-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="c455b-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="c455b-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c455b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c455b-106">Fonction de bibliothèque Framework crée un temporaire **XLOPER**/ **XLOPER12** de type **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="c455b-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="c455b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c455b-107">Parameters</span></span>

<span data-ttu-id="c455b-108">Cette fonction n’utilise aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c455b-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c455b-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c455b-109">Return value</span></span>

<span data-ttu-id="c455b-110">Retourne un pointeur vers une **xltypeMissing** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="c455b-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="c455b-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="c455b-111">Example</span></span>

<span data-ttu-id="c455b-112">Cet exemple utilise **TempMissing12** pour fournir trois arguments manquants à **xlcWorkspace** suivi d’un **Boolean** **FALSE** pour supprimer l’affichage des barres de défilement de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="c455b-112">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars.</span></span> <span data-ttu-id="c455b-113">Les trois premiers arguments correspondent aux autres paramètres de l’espace de travail qui ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="c455b-113">The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c455b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c455b-114">See also</span></span>



[<span data-ttu-id="c455b-115">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="c455b-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

