---
title: Définir des propriétés de formulaire, d'état et de contrôle
TOCTitle: Set form, report, and control properties
description: Chaque formulaire, état, section et contrôle possèdent des paramètres de propriété que vous pouvez définir pour modifier l’apparence ou le comportement d’un élément particulier dans Access 2013.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2ffb02f78bbf9d9f4c5d5b07c1ee08e3f19453b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874603"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="596c2-103">Définir des propriétés de formulaire, d'état et de contrôle</span><span class="sxs-lookup"><span data-stu-id="596c2-103">Set form, report, and control properties</span></span>

<span data-ttu-id="596c2-104">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="596c2-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="596c2-p101">Chaque formulaire, état, section et contrôle possède des paramètres de propriété que vous pouvez définir pour modifier l'aspect ou le fonctionnement de cet élément particulier. Vous pouvez afficher et modifier les propriétés à l'aide de la feuille des propriétés, d'une macro ou de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="596c2-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="596c2-107">Définition des propriétés</span><span class="sxs-lookup"><span data-stu-id="596c2-107">Set properties</span></span>

1. <span data-ttu-id="596c2-p102">En mode Création de formulaire ou d'état, sélectionnez le contrôle, la section, le formulaire ou l'état dont vous voulez définir la propriété. Vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="596c2-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="596c2-110">Un ou plusieurs contrôles.</span><span class="sxs-lookup"><span data-stu-id="596c2-110">One or more controls.</span></span> <span data-ttu-id="596c2-111">Pour sélectionner plusieurs contrôles, maintenez la touche MAJ enfoncée et sélectionnez les contrôles ou faites glisser le pointeur de la souris sur les contrôles que vous souhaitez sélectionner.</span><span class="sxs-lookup"><span data-stu-id="596c2-111">To select multiple controls, hold down the SHIFT key and choose the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="596c2-112">Si vous sélectionnez plusieurs contrôles, la feuille des propriétés n'affiche que les propriétés communes aux contrôles sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="596c2-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="596c2-113">Une section.</span><span class="sxs-lookup"><span data-stu-id="596c2-113">One section.</span></span> <span data-ttu-id="596c2-114">Cliquez sur le sélecteur de section de la section que vous souhaitez sélectionner.</span><span class="sxs-lookup"><span data-stu-id="596c2-114">Choose the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="596c2-115">Le formulaire ou l'état entier.</span><span class="sxs-lookup"><span data-stu-id="596c2-115">The entire form or report.</span></span> <span data-ttu-id="596c2-116">Cliquez sur le sélecteur de formulaire ou état dans le coin supérieur gauche du formulaire ou du rapport.</span><span class="sxs-lookup"><span data-stu-id="596c2-116">Choose the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="596c2-117">Afficher la feuille des propriétés, avec le bouton droit de l’objet ou la section, puis choisissez **Propriétés** dans le menu contextuel ou en cliquant sur **Propriétés** dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="596c2-117">Display the property sheet by right-clicking the object or section and then choosing **Properties** on the shortcut menu, or by choosing **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="596c2-118">Choisissez la propriété pour laquelle vous voulez définir la valeur, puis effectuez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="596c2-118">Choose the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="596c2-119">Dans la zone de propriété, tapez le paramètre ou l'expression approprié.</span><span class="sxs-lookup"><span data-stu-id="596c2-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="596c2-120">Si la zone de propriété comporte une flèche, cliquez sur la flèche, puis choisissez une valeur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="596c2-120">If the property box contains an arrow, choose the arrow and then choose a value in the list.</span></span>
    
   - <span data-ttu-id="596c2-121">Si un bouton **Générer** apparaît à droite de la zone de propriété, cliquez dessus pour afficher un générateur ou pour afficher une boîte de dialogue vous offrant un choix de générateurs.</span><span class="sxs-lookup"><span data-stu-id="596c2-121">If a **Build** button appears to the right of the property box, choose it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="596c2-122">Par exemple, vous pouvez utiliser le Générateur de code, le Générateur de macro ou le Générateur de requêtes pour définir des propriétés.</span><span class="sxs-lookup"><span data-stu-id="596c2-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="596c2-123">Conseils</span><span class="sxs-lookup"><span data-stu-id="596c2-123">Tips</span></span>

- <span data-ttu-id="596c2-124">Microsoft Access comporte une zone de **Zoom** qui permet de taper et d'afficher des expressions ou d'autres paramètres de propriété longs.</span><span class="sxs-lookup"><span data-stu-id="596c2-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="596c2-125">Pour afficher la zone **Zoom** , choisissez une zone de propriété dans la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="596c2-125">To display the **Zoom** box, choose a property box in the property sheet.</span></span> <span data-ttu-id="596c2-126">Appuyez sur MAJ + F2 ou avec le bouton droit, puis choisissez **Zoom** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="596c2-126">Press SHIFT+F2, or right-click, and then choose **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="596c2-127">Vous pouvez définir la propriété **ControlSource** pour certains contrôles en tapant le paramètre de propriété dans le contrôle lui-même.</span><span class="sxs-lookup"><span data-stu-id="596c2-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="596c2-128">Vous pouvez modifier les paramètres de propriété par défaut pour un type de contrôle de manière à ce que les contrôles que vous créez possèdent les nouveaux paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="596c2-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="596c2-129">Les paramètres de propriété d'un contrôle dépendant risquent de ne pas correspondre aux paramètres correspondants du champ de la table ou requête sous-jacente à laquelle le contrôle est associé.</span><span class="sxs-lookup"><span data-stu-id="596c2-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="596c2-130">Si les paramètres sont différents, les paramètres du formulaire ou de l'état annulent généralement ceux de la table ou de la requête.</span><span class="sxs-lookup"><span data-stu-id="596c2-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

