---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782238"
---
# <a name="xlfgetdef"></a><span data-ttu-id="d111e-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="d111e-104">xlfGetDef</span></span>

<span data-ttu-id="d111e-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d111e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d111e-106">Renvoie le nom, sous forme de texte, qui est défini pour une zone particulière, une valeur ou une formule dans un classeur.</span><span class="sxs-lookup"><span data-stu-id="d111e-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="d111e-107">Dans Excel, cette valeur est affichée dans la colonne **nom** de la boîte de dialogue **Gestionnaire de noms** qui s’affiche lorsque vous cliquez sur **Gestionnaire de noms** dans la section **Noms définis** sous l’onglet **formules** utiliser **xlfGetDef** pour obtenir le nom qui correspond à une définition.</span><span class="sxs-lookup"><span data-stu-id="d111e-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="d111e-108">Pour obtenir la définition d’un nom, utilisez [xlfGetName](xlfgetname.md).</span><span class="sxs-lookup"><span data-stu-id="d111e-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="d111e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d111e-109">Parameters</span></span>

<span data-ttu-id="d111e-110">_pxDefText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="d111e-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d111e-111">Peut être tout ce que vous pouvez définir un nom pour faire référence à, y compris une référence, une valeur, un objet ou une formule.</span><span class="sxs-lookup"><span data-stu-id="d111e-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="d111e-112">Références doivent figurer dans le style R1C1, tel que `"R3C5"`.</span><span class="sxs-lookup"><span data-stu-id="d111e-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="d111e-113">Si _pxDefText_ est une valeur ou une formule, il n’est pas nécessaire d’inclure le signe égal qui est affiché dans la colonne **Fait référence à** la boîte de dialogue **Gestionnaire de noms** .</span><span class="sxs-lookup"><span data-stu-id="d111e-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="d111e-114">S’il existe plusieurs noms pour _pxDefText_, **xlfGetDef** renvoie le premier nom.</span><span class="sxs-lookup"><span data-stu-id="d111e-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="d111e-115">Si aucun nom correspond à _pxDefText_, **xlfGetDef** renvoie la `#NAME?` valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d111e-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="d111e-116">_pxDocumentText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="d111e-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d111e-117">Spécifie la feuille qui _pxDefText_ se trouve sur.</span><span class="sxs-lookup"><span data-stu-id="d111e-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="d111e-118">Si _pxDocumentText_ est omis, il est supposé pour être la feuille active.</span><span class="sxs-lookup"><span data-stu-id="d111e-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="d111e-119">_pxTypeNum_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="d111e-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="d111e-120">Nombre compris entre 1 et 3 spécifiant les types de noms sont retournés.</span><span class="sxs-lookup"><span data-stu-id="d111e-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="d111e-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="d111e-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="d111e-122">**Renvoie**</span><span class="sxs-lookup"><span data-stu-id="d111e-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d111e-123">1 ou aucune</span><span class="sxs-lookup"><span data-stu-id="d111e-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="d111e-124">Noms normales uniquement.</span><span class="sxs-lookup"><span data-stu-id="d111e-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="d111e-125">2</span><span class="sxs-lookup"><span data-stu-id="d111e-125">2</span></span>  <br/> |<span data-ttu-id="d111e-126">Noms masqués.</span><span class="sxs-lookup"><span data-stu-id="d111e-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="d111e-127">3</span><span class="sxs-lookup"><span data-stu-id="d111e-127">3</span></span>  <br/> |<span data-ttu-id="d111e-128">Tous les noms.</span><span class="sxs-lookup"><span data-stu-id="d111e-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="d111e-129">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d111e-129">Property value/Return value</span></span>

 <span data-ttu-id="d111e-130">_pxRes_ (**xltypeStr** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="d111e-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="d111e-131">Renvoie le nom associé à la définition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d111e-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d111e-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="d111e-132">Remarks</span></span>

<span data-ttu-id="d111e-133">Le tableau suivant répertorie les quatre exemples des valeurs renvoyées par un appel à **xlfGetDef** avec les arguments spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d111e-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="d111e-134">**Nom défini dans Excel**</span><span class="sxs-lookup"><span data-stu-id="d111e-134">**Name defined in Excel**</span></span>|<span data-ttu-id="d111e-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="d111e-135">**_pxDefText_**</span></span>|<span data-ttu-id="d111e-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="d111e-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="d111e-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="d111e-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="d111e-138">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="d111e-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d111e-139">La plage spécifiée dans Sheet4 est nommée Ventes.</span><span class="sxs-lookup"><span data-stu-id="d111e-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="d111e-140">« R2C2:R9C6 »</span><span class="sxs-lookup"><span data-stu-id="d111e-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="d111e-141">« Sheet4 »</span><span class="sxs-lookup"><span data-stu-id="d111e-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="d111e-142">\<omis\></span><span class="sxs-lookup"><span data-stu-id="d111e-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="d111e-143">« Ventes »</span><span class="sxs-lookup"><span data-stu-id="d111e-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="d111e-144">La valeur 100 Sheet4 est définie comme constante.</span><span class="sxs-lookup"><span data-stu-id="d111e-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="d111e-145">« 100 »</span><span class="sxs-lookup"><span data-stu-id="d111e-145">"100"</span></span>  <br/> |<span data-ttu-id="d111e-146">« Sheet4 »</span><span class="sxs-lookup"><span data-stu-id="d111e-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="d111e-147">\<omis\></span><span class="sxs-lookup"><span data-stu-id="d111e-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="d111e-148">« Constante »</span><span class="sxs-lookup"><span data-stu-id="d111e-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="d111e-149">La formule spécifiée dans Sheet4 est nommée SumTotal.</span><span class="sxs-lookup"><span data-stu-id="d111e-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="d111e-150">« SUM(R1C1:R10C1) »</span><span class="sxs-lookup"><span data-stu-id="d111e-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="d111e-151">« Sheet4 »</span><span class="sxs-lookup"><span data-stu-id="d111e-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="d111e-152">\<omis\></span><span class="sxs-lookup"><span data-stu-id="d111e-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="d111e-153">« SumTotal »</span><span class="sxs-lookup"><span data-stu-id="d111e-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="d111e-154">3 est défini comme nom masqué compteur dans la feuille active.</span><span class="sxs-lookup"><span data-stu-id="d111e-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="d111e-155">« 3 »</span><span class="sxs-lookup"><span data-stu-id="d111e-155">"3"</span></span>  <br/> |<span data-ttu-id="d111e-156">\<omis\></span><span class="sxs-lookup"><span data-stu-id="d111e-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="d111e-157">2</span><span class="sxs-lookup"><span data-stu-id="d111e-157">2</span></span>  <br/> |<span data-ttu-id="d111e-158">« Compteur »</span><span class="sxs-lookup"><span data-stu-id="d111e-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d111e-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d111e-159">See also</span></span>

- [<span data-ttu-id="d111e-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="d111e-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="d111e-161">Fonctions XLM API C essentielles et utiles</span><span class="sxs-lookup"><span data-stu-id="d111e-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

