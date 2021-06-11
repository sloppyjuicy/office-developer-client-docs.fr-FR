---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436628"
---
# <a name="xlfgetname"></a><span data-ttu-id="d62be-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="d62be-104">xlfGetName</span></span>

<span data-ttu-id="d62be-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d62be-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d62be-106">Renvoie la définition d’un nom tel qu’il  apparaît dans la colonne **Références**  de la boîte de dialogue Gestionnaire de noms, qui s’affiche lorsque vous cliquez sur Gestionnaire de noms dans la **section** Noms définis sous l’onglet **Formules.** Si la définition contient des références, elles sont données en tant que références de style R1C1.</span><span class="sxs-lookup"><span data-stu-id="d62be-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="d62be-107">Utilisez **xlfGetName pour vérifier** la valeur définie par un nom.</span><span class="sxs-lookup"><span data-stu-id="d62be-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="d62be-108">Pour obtenir le nom qui correspond à une définition, utilisez [xlfGetDef](xlfgetdef.md).</span><span class="sxs-lookup"><span data-stu-id="d62be-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="d62be-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="d62be-109">Parameters</span></span>

<span data-ttu-id="d62be-110">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="d62be-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d62be-111">Il peut s’agit d’un nom défini dans la feuille . une référence externe à un nom défini dans le livre de travail actif, par exemple, ou une référence externe à un nom défini sur un workbook ouvert  `"!Sales"` particulier, par exemple,  `"[Book1]SHEET1!Sales"` .</span><span class="sxs-lookup"><span data-stu-id="d62be-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="d62be-112">_pxNameText_ peut également être un nom masqué.</span><span class="sxs-lookup"><span data-stu-id="d62be-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="d62be-113">_pxInfoType_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="d62be-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="d62be-114">Spécifie le type d’informations à renvoyer sur le nom.</span><span class="sxs-lookup"><span data-stu-id="d62be-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="d62be-115">Si **false** ou omis, la définition est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="d62be-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="d62be-116">Si **true**, renvoie **TRUE** si le nom est défini uniquement pour la feuille, **FALSE** si le nom est défini pour l’ensemble du workbook.</span><span class="sxs-lookup"><span data-stu-id="d62be-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d62be-117">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="d62be-117">Property value/Return value</span></span>

<span data-ttu-id="d62be-118">_pxRes_ (**xltypeStr**, **xltypeBool** ou **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="d62be-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="d62be-119">En fonction de la valeur passée pour  _pxInfoType_, renvoie la définition du nom spécifié (**xltypeStr**), ou **TRUE** ou **FALSE** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="d62be-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d62be-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="d62be-120">Remarks</span></span>

<span data-ttu-id="d62be-121">Si  la case à cocher Protéger la feuille de  calcul et le contenu des cellules verrouillées a été sélectionnée dans la boîte de dialogue Protéger la feuille pour protéger le workbook contenant le nom, **xlfGetName** renvoie la valeur `#N/A` d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d62be-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="d62be-122">Pour voir la boîte **de dialogue Protéger la feuille,** cliquez sur Protéger la **feuille** dans la section **Modifications** de **l’onglet** Révision.</span><span class="sxs-lookup"><span data-stu-id="d62be-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="d62be-123">Le tableau suivant répertorie trois exemples de valeurs renvoyées par un appel à **xlfGetDef** avec l’argument  _pxNameText_ spécifié.</span><span class="sxs-lookup"><span data-stu-id="d62be-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="d62be-124">**Définition dans Excel**</span><span class="sxs-lookup"><span data-stu-id="d62be-124">**Definition in Excel**</span></span>|<span data-ttu-id="d62be-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="d62be-125">**_pxNameText_**</span></span>|<span data-ttu-id="d62be-126">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="d62be-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d62be-127">Le nom Ventes sur une feuille est défini comme le numéro 523.</span><span class="sxs-lookup"><span data-stu-id="d62be-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="d62be-128">« Ventes »</span><span class="sxs-lookup"><span data-stu-id="d62be-128">"Sales"</span></span>  <br/> |<span data-ttu-id="d62be-129">« =523 »</span><span class="sxs-lookup"><span data-stu-id="d62be-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="d62be-130">Le nom Profit de la feuille active est défini comme la formule =Sales-Costs.</span><span class="sxs-lookup"><span data-stu-id="d62be-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="d62be-131">"! Profit »</span><span class="sxs-lookup"><span data-stu-id="d62be-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="d62be-132">« =Sales-Costs »</span><span class="sxs-lookup"><span data-stu-id="d62be-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="d62be-133">Le nom Base de données de la feuille active est défini comme la plage A1:F500.</span><span class="sxs-lookup"><span data-stu-id="d62be-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="d62be-134">"! Base de données »</span><span class="sxs-lookup"><span data-stu-id="d62be-134">"!Database"</span></span>  <br/> |<span data-ttu-id="d62be-135">« =R1C1:R500C6 »</span><span class="sxs-lookup"><span data-stu-id="d62be-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d62be-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d62be-136">See also</span></span>

- [<span data-ttu-id="d62be-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="d62be-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="d62be-138">Fonctions XLM essentielles et utiles de l’API C</span><span class="sxs-lookup"><span data-stu-id="d62be-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

