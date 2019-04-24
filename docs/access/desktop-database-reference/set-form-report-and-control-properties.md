---
title: Définir des propriétés de formulaire, de rapport et de contrôle
TOCTitle: Set form, report, and control properties
description: Chaque formulaire, rapport, section et contrôle possède des paramètres de propriété que vous pouvez définir pour modifier l'aspect ou le fonctionnement de cet élément particulier dans Access 2013.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: bacbdc100d147be8bf4327a5a775b199c79347bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308735"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="bd0f0-103">Définir des propriétés de formulaire, de rapport et de contrôle</span><span class="sxs-lookup"><span data-stu-id="bd0f0-103">Set form, report, and control properties</span></span>

<span data-ttu-id="bd0f0-104">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd0f0-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd0f0-p101">Chaque formulaire, état, section et contrôle possède des paramètres de propriété que vous pouvez définir pour modifier l'aspect ou le fonctionnement de cet élément particulier. Vous pouvez afficher et modifier les propriétés à l'aide de la feuille des propriétés, d'une macro ou de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="bd0f0-107">Définition des propriétés</span><span class="sxs-lookup"><span data-stu-id="bd0f0-107">Set properties</span></span>

1. <span data-ttu-id="bd0f0-p102">En mode Création de formulaire ou d'état, sélectionnez le contrôle, la section, le formulaire ou l'état dont vous voulez définir la propriété. Vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="bd0f0-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="bd0f0-110">Un ou plusieurs contrôles.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-110">One or more controls.</span></span> <span data-ttu-id="bd0f0-111">Pour sélectionner plusieurs contrôles, vous pouvez cliquer sur des contrôles en maintenant la touche Maj enfoncée ou vous pouvez cliquer et faire glisser le pointeur de la souris sur les contrôles à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-111">To select multiple controls, hold down the SHIFT key and click the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="bd0f0-112">Si vous sélectionnez plusieurs contrôles, la feuille des propriétés n'affiche que les propriétés communes aux contrôles sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="bd0f0-113">Une section.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-113">One section.</span></span> <span data-ttu-id="bd0f0-114">Cliquez sur le sélecteur de section de la section que vous voulez sélectionner.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-114">Click the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="bd0f0-115">Ensemble du formulaire ou rapport.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-115">The entire form or report.</span></span> <span data-ttu-id="bd0f0-116">Cliquez sur le sélecteur de formulaire ou le sélecteur de rapport dans le coin supérieur du formulaire ou du rapport.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-116">Click the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="bd0f0-117">Affichez la feuille des propriétés en cliquant à l'aide du bouton droit de la souris sur l'objet ou la section, puis en cliquant sur **Propriétés** dans le menu contextuel ou en cliquant sur **Propriétés** dans la barre d'outils.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-117">Display the property sheet by right-clicking the object or section and then clicking **Properties** on the shortcut menu, or by clicking **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="bd0f0-118">Cliquez sur la propriété dont vous voulez définir la valeur, puis exécutez une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd0f0-118">Click the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="bd0f0-119">Dans la zone de propriété, tapez l’expression ou paramètre approprié.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="bd0f0-120">Si la zone de propriété comporte une flèche, cliquez sur cette dernière et choisissez une valeur dans la liste.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-120">If the property box contains an arrow, click the arrow and then click a value in the list.</span></span>
    
   - <span data-ttu-id="bd0f0-121">Si un bouton **Générer** apparaît à droite de la zone de propriété, cliquez dessus pour afficher un générateur ou pour afficher une boîte de dialogue vous offrant un choix de générateurs.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-121">If a **Build** button appears to the right of the property box, click it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="bd0f0-122">Par exemple, vous pouvez utiliser le Générateur de Code, le Générateur de Macro ou le Générateur de requêtes pour définir certaines propriétés.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="bd0f0-123">Conseils </span><span class="sxs-lookup"><span data-stu-id="bd0f0-123">Tips</span></span>

- <span data-ttu-id="bd0f0-124">Microsoft Access vous propose une zone **Zoom** pour taper et afficher des expressions ou autres paramètres de propriété longue.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="bd0f0-125">Pour afficher la zone de **Zoom**, cliquez sur une zone de propriété dans la feuille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-125">To display the **Zoom** box, click a property box in the property sheet.</span></span> <span data-ttu-id="bd0f0-126">Ensuite, appuyez sur Maj+F2 ou cliquez sur le bouton droit de la souris et choisissez **Zoom** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-126">Then press SHIFT+F2, or right-click and then click **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="bd0f0-127">Vous pouvez définir la propriété **ControlSource** pour certains contrôles en tapant le paramètre de propriété dans le contrôle lui-même.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="bd0f0-128">Vous pouvez modifier les paramètres de propriété par défaut pour un type de contrôle de manière à ce que les contrôles que vous créez possèdent les nouveaux paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="bd0f0-129">Les paramètres de propriété d'un contrôle dépendant risquent de ne pas correspondre aux paramètres correspondants du champ de la table ou requête sous-jacente à laquelle le contrôle est associé.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="bd0f0-130">Si les paramètres sont différents, les paramètres du formulaire ou de l'état annulent généralement ceux de la table ou de la requête.</span><span class="sxs-lookup"><span data-stu-id="bd0f0-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

