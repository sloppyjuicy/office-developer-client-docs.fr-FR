---
title: GoToPage, action de macro
TOCTitle: GoToPage macro action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 10d55b435a59594eaf3e8380b6690ebbda63a258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292159"
---
# <a name="gotopage-macro-action"></a><span data-ttu-id="de96e-102">GoToPage, action de macro</span><span class="sxs-lookup"><span data-stu-id="de96e-102">GoToPage macro action</span></span>

<span data-ttu-id="de96e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de96e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de96e-p101">Utilisez l'action **AtteindrePage** pour placer le focus dans le formulaire actif sur le premier contrôle d'une page spécifique. Vous pouvez utiliser cette action si vous avez créé un formulaire contenant différents groupes d'informations connexes séparés par des sauts de page. Par exemple, un formulaire Employés peut contenir des informations personnelles sur une page, des informations professionnelles sur une autre page et des informations sur les ventes sur une troisième page. Vous pouvez utiliser l'action **AtteindrePage** pour vous placer sur la page de votre choix. Vous pouvez également présenter plusieurs pages d'informations sur un même formulaire en utilisant des contrôles Onglet.</span><span class="sxs-lookup"><span data-stu-id="de96e-p101">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page. You can use this action if you have created a form with page breaks that contains groups of related information. For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page. You can use the **GoToPage** action to move to the desired page. You can also present multiple pages of information on a single form by using tab controls.</span></span>

## <a name="setting"></a><span data-ttu-id="de96e-109">Setting</span><span class="sxs-lookup"><span data-stu-id="de96e-109">Setting</span></span>

<span data-ttu-id="de96e-110">L’action **AtteindrePage** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="de96e-110">The **GoToPage** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de96e-111">Argument d’action</span><span class="sxs-lookup"><span data-stu-id="de96e-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="de96e-112">Description</span><span class="sxs-lookup"><span data-stu-id="de96e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de96e-113"><strong>Numéro de page</strong></span><span class="sxs-lookup"><span data-stu-id="de96e-113"><strong>Page Number</strong></span></span></p></td>
<td><p><span data-ttu-id="de96e-p102">Numéro de la page sur laquelle placer le focus. Entrez le numéro de la page dans la zone <strong>Numéro de page</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Si vous laissez cet argument vide, le focus reste sur la page active. Vous pouvez utiliser les arguments <strong>Droite</strong> et <strong>Bas</strong> pour afficher la partie de la page qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="de96e-p102">The number of the page to which you want to move the focus. Enter the page number in the <strong>Page Number</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. If you leave this argument blank, the focus stays on the current page. You can use the <strong>Right</strong> and <strong>Down</strong> arguments to display the part of the page you want to see.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de96e-118"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="de96e-118"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="de96e-p103">Position horizontale de la partie de la page, mesurée à partir du bord gauche de la fenêtre principale, qui doit apparaître sur le bord gauche de la fenêtre. Cet argument est obligatoire si l’argument <strong>Bas</strong> est spécifié.</span><span class="sxs-lookup"><span data-stu-id="de96e-p103">The horizontal position of the spot on the page, measured from the left edge of its containing window, that is to appear at the left edge of the window. This is required if you specify a <strong>Down</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de96e-121"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="de96e-121"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="de96e-p104">Position verticale de la partie de la page, mesurée à partir du bord supérieur de la fenêtre principale, qui doit apparaître sur le bord supérieur de la fenêtre. Cet argument est obligatoire si l’argument <strong>Haut</strong> est spécifié.</span><span class="sxs-lookup"><span data-stu-id="de96e-p104">The vertical position of the spot on the page, measured from the top edge of its containing window, that is to appear at the top edge of the window. This is required if you specify a <strong>Right</strong> argument.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="de96e-124">Les arguments **Droite** et **Bas** sont mesurés en pouces ou en centimètres, selon les paramètres régionaux définis dans le Panneau de configuration de Windows.</span><span class="sxs-lookup"><span data-stu-id="de96e-124">The **Right** and **Down** arguments are measured in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="de96e-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="de96e-125">Remarks</span></span>

<span data-ttu-id="de96e-p105">Vous pouvez utiliser cette action pour sélectionner le premier contrôle (comme défini par l’ordre de tabulation du formulaire) sur la page spécifiée. Utilisez l’action **AtteindreContrôle** pour vous placer dans un contrôle particulier sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="de96e-p105">You can use this action to select the first control (as defined by the form's tab order) on the specified page. Use the **GoToControl** action to move to a particular control on the form.</span></span>

<span data-ttu-id="de96e-128">Vous pouvez utiliser les arguments **droite** et **bas** pour les formulaires dont la taille des pages est supérieure à celle de la fenêtre Access.</span><span class="sxs-lookup"><span data-stu-id="de96e-128">You can use the **Right** and **Down** arguments for forms with pages larger than the Access window.</span></span> <span data-ttu-id="de96e-129">Utilisez l'argument **Numéro de page** pour vous placer sur la page de votre choix, puis utilisez les arguments **Droite** et **Bas** pour afficher la partie de la page de votre choix.</span><span class="sxs-lookup"><span data-stu-id="de96e-129">Use the **Page Number** argument to move to the desired page, and then use the **Right** and **Down** arguments to display the part of the page you want to see.</span></span> <span data-ttu-id="de96e-130">Access affiche la partie de la page dont l'angle supérieur gauche est décalé de la distance spécifiée de l'angle supérieur gauche de la page.</span><span class="sxs-lookup"><span data-stu-id="de96e-130">Access displays the part of the page whose upper-left corner is offset the specified distance from the upper-left corner of the page.</span></span>

<span data-ttu-id="de96e-131">Vous pouvez utiliser l'action **AtteindrePage** dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="de96e-131">You can't use the **GoToPage** action in the following cases:</span></span>

- <span data-ttu-id="de96e-132">pour placer le focus sur une page dans un formulaire masqué ;</span><span class="sxs-lookup"><span data-stu-id="de96e-132">To move the focus to a page on a hidden form.</span></span>

- <span data-ttu-id="de96e-133">pour placer le focus sur une autre page dans le contrôle Onglet.</span><span class="sxs-lookup"><span data-stu-id="de96e-133">To move the focus from one page to another within the tab control.</span></span>

<span data-ttu-id="de96e-134">Pour exécuter l'action **AtteindrePage** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **GoToPage** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="de96e-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span></span>

