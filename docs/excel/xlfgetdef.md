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
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421997"
---
# <a name="xlfgetdef"></a><span data-ttu-id="592b5-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="592b5-104">xlfGetDef</span></span>

<span data-ttu-id="592b5-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="592b5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="592b5-106">Renvoie le nom, en tant que texte, qui est défini pour une zone, une valeur ou une formule particulière dans un workbook.</span><span class="sxs-lookup"><span data-stu-id="592b5-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="592b5-107">Dans Excel, cette valeur est affichée dans  la colonne Nom de la boîte  de dialogue Gestionnaire de noms, qui s’affiche lorsque vous cliquez sur Gestionnaire de noms dans la **section** Noms définis sous l’onglet **Formules.**  Utilisez **xlfGetDef** pour obtenir le nom qui correspond à une définition.</span><span class="sxs-lookup"><span data-stu-id="592b5-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="592b5-108">Pour obtenir la définition d’un nom, utilisez [xlfGetName](xlfgetname.md).</span><span class="sxs-lookup"><span data-stu-id="592b5-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="592b5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="592b5-109">Parameters</span></span>

<span data-ttu-id="592b5-110">_pxDefText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="592b5-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="592b5-111">Il peut s’agit de tout ce à quoi vous pouvez définir un nom à référencer, y compris une référence, une valeur, un objet ou une formule.</span><span class="sxs-lookup"><span data-stu-id="592b5-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="592b5-112">Les références doivent être données dans le style R1C1, par  `"R3C5"` exemple.</span><span class="sxs-lookup"><span data-stu-id="592b5-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="592b5-113">Si  _pxDefText_ est une valeur ou une formule, il n’est pas nécessaire d’inclure le signe égal affiché dans la colonne **Références** dans la boîte de dialogue **Gestionnaire** de noms.</span><span class="sxs-lookup"><span data-stu-id="592b5-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="592b5-114">S’il existe plusieurs noms  _pour pxDefText_, **xlfGetDef** renvoie le prénom.</span><span class="sxs-lookup"><span data-stu-id="592b5-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="592b5-115">Si aucun nom ne correspond  _à pxDefText_, **xlfGetDef** renvoie la valeur  `#NAME?` d’erreur.</span><span class="sxs-lookup"><span data-stu-id="592b5-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="592b5-116">_pxDocumentText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="592b5-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="592b5-117">Spécifie la feuille sur qui se trouve _pxDefText._</span><span class="sxs-lookup"><span data-stu-id="592b5-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="592b5-118">Si  _pxDocumentText_ est omis, il est supposé être la feuille active.</span><span class="sxs-lookup"><span data-stu-id="592b5-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="592b5-119">_pxTypeNum_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="592b5-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="592b5-120">Nombre de 1 à 3 spécifiant les types de noms renvoyés.</span><span class="sxs-lookup"><span data-stu-id="592b5-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="592b5-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="592b5-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="592b5-122">**Renvoie**</span><span class="sxs-lookup"><span data-stu-id="592b5-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="592b5-123">1 ou aucune</span><span class="sxs-lookup"><span data-stu-id="592b5-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="592b5-124">Noms normaux uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b5-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="592b5-125">2 </span><span class="sxs-lookup"><span data-stu-id="592b5-125">2</span></span>  <br/> |<span data-ttu-id="592b5-126">Noms masqués uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b5-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="592b5-127">3 </span><span class="sxs-lookup"><span data-stu-id="592b5-127">3</span></span>  <br/> |<span data-ttu-id="592b5-128">Tous les noms.</span><span class="sxs-lookup"><span data-stu-id="592b5-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="592b5-129">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="592b5-129">Property value/Return value</span></span>

 <span data-ttu-id="592b5-130">_pxRes_ (**xltypeStr** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="592b5-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="592b5-131">Renvoie le nom associé à la définition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="592b5-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="592b5-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="592b5-132">Remarks</span></span>

<span data-ttu-id="592b5-133">Le tableau suivant répertorie quatre exemples de valeurs renvoyées par un appel à **xlfGetDef** avec les arguments spécifiés.</span><span class="sxs-lookup"><span data-stu-id="592b5-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="592b5-134">**Nom défini dans Excel**</span><span class="sxs-lookup"><span data-stu-id="592b5-134">**Name defined in Excel**</span></span>|<span data-ttu-id="592b5-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="592b5-135">**_pxDefText_**</span></span>|<span data-ttu-id="592b5-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="592b5-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="592b5-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="592b5-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="592b5-138">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="592b5-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="592b5-139">La plage spécifiée dans la feuille Sheet4 est nommée Ventes.</span><span class="sxs-lookup"><span data-stu-id="592b5-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="592b5-140">« R2C2:R9C6 »</span><span class="sxs-lookup"><span data-stu-id="592b5-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="592b5-141">« Sheet4 »</span><span class="sxs-lookup"><span data-stu-id="592b5-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="592b5-142">\<omis\></span><span class="sxs-lookup"><span data-stu-id="592b5-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="592b5-143">« Ventes »</span><span class="sxs-lookup"><span data-stu-id="592b5-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="592b5-144">La valeur 100 dans la feuille Sheet4 est définie comme Constante.</span><span class="sxs-lookup"><span data-stu-id="592b5-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="592b5-145">"100"</span><span class="sxs-lookup"><span data-stu-id="592b5-145">"100"</span></span>  <br/> |<span data-ttu-id="592b5-146">« Sheet4 »</span><span class="sxs-lookup"><span data-stu-id="592b5-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="592b5-147">\<omis\></span><span class="sxs-lookup"><span data-stu-id="592b5-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="592b5-148">« Constante »</span><span class="sxs-lookup"><span data-stu-id="592b5-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="592b5-149">La formule spécifiée dans la feuille Sheet4 est nommée SumTotal.</span><span class="sxs-lookup"><span data-stu-id="592b5-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="592b5-150">« SUM(R1C1:R10C1) »</span><span class="sxs-lookup"><span data-stu-id="592b5-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="592b5-151">« Sheet4 »</span><span class="sxs-lookup"><span data-stu-id="592b5-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="592b5-152">\<omis\></span><span class="sxs-lookup"><span data-stu-id="592b5-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="592b5-153">« SumTotal »</span><span class="sxs-lookup"><span data-stu-id="592b5-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="592b5-154">3 est défini comme le compteur de nom masqué dans la feuille active.</span><span class="sxs-lookup"><span data-stu-id="592b5-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="592b5-155">"3"</span><span class="sxs-lookup"><span data-stu-id="592b5-155">"3"</span></span>  <br/> |<span data-ttu-id="592b5-156">\<omis\></span><span class="sxs-lookup"><span data-stu-id="592b5-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="592b5-157">2 </span><span class="sxs-lookup"><span data-stu-id="592b5-157">2</span></span>  <br/> |<span data-ttu-id="592b5-158">« Counter »</span><span class="sxs-lookup"><span data-stu-id="592b5-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="592b5-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="592b5-159">See also</span></span>

- [<span data-ttu-id="592b5-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="592b5-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="592b5-161">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="592b5-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

