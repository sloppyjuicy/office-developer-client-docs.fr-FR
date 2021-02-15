---
title: PrintOut, action de macro
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 04212a8bf63d5039c6548463612f006f0d116229
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301406"
---
# <a name="printout-macro-action"></a><span data-ttu-id="5ba80-102">PrintOut, action de macro</span><span class="sxs-lookup"><span data-stu-id="5ba80-102">PrintOut macro action</span></span>

<span data-ttu-id="5ba80-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ba80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ba80-p101">Faites appel à l'action **Imprimer** pour imprimer l'objet actif dans la base de données ouverte. Vous pouvez imprimer des feuilles de données, des états, des formulaires, des pages d'accès aux données et des modules.</span><span class="sxs-lookup"><span data-stu-id="5ba80-p101">You can use the **PrintOut** action to print the active object in the open database. You can print datasheets, reports, forms, data access pages, and modules.</span></span>

> [!NOTE]
> <span data-ttu-id="5ba80-106">Cette action ne sera pas autorisée si la base de données n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="5ba80-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="5ba80-107">Setting</span><span class="sxs-lookup"><span data-stu-id="5ba80-107">Setting</span></span>

<span data-ttu-id="5ba80-108">L’action **Imprimer** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="5ba80-108">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ba80-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="5ba80-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5ba80-110">Description</span><span class="sxs-lookup"><span data-stu-id="5ba80-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ba80-111"><strong>Imprimer</strong></span><span class="sxs-lookup"><span data-stu-id="5ba80-111"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba80-p102">Étendue d’impression. Cliquez sur <strong>Tout</strong> (l’utilisateur peut imprimer l’intégralité de l’objet), sur <strong>Sélection</strong> (l’utilisateur peut imprimer la partie de l’objet qui est sélectionnée) ou sur <strong>Pages</strong> (l’utilisateur peut spécifier une série de pages dans les arguments <strong>De la page</strong> et <strong>À la page</strong>) dans la zone <strong>Imprimer</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. La valeur par défaut est <strong>Tout</strong>.</span><span class="sxs-lookup"><span data-stu-id="5ba80-p102">The range to print. Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba80-115"><strong>De la page</strong></span><span class="sxs-lookup"><span data-stu-id="5ba80-115"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba80-p103">Première page à imprimer. L’impression commence en haut de cette page. Cet argument est obligatoire si vous sélectionnez l’option <strong>Pages</strong> dans la zone <strong>Imprimer</strong>.</span><span class="sxs-lookup"><span data-stu-id="5ba80-p103">The first page to print. Printing starts at the top of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba80-119"><strong>À la page</strong></span><span class="sxs-lookup"><span data-stu-id="5ba80-119"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba80-p104">Dernière page à imprimer. L’impression s’arrête à la fin de cette page. Cet argument est obligatoire si vous sélectionnez l’option <strong>Pages</strong> dans la zone <strong>Imprimer</strong>.</span><span class="sxs-lookup"><span data-stu-id="5ba80-p104">The last page to print. Printing stops at the bottom of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba80-123"><strong>Qualité de l’impression</strong></span><span class="sxs-lookup"><span data-stu-id="5ba80-123"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba80-124">Qualité d’impression.</span><span class="sxs-lookup"><span data-stu-id="5ba80-124">The print quality.</span></span> <span data-ttu-id="5ba80-125">Cliquez sur <strong>Haute</strong>, <strong>Moyenne</strong>, <strong>Basse</strong> ou <strong>Brouillon</strong>.</span><span class="sxs-lookup"><span data-stu-id="5ba80-125">Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>.</span></span> <span data-ttu-id="5ba80-126">Plus la qualité est basse, plus l’impression de l’objet est rapide.</span><span class="sxs-lookup"><span data-stu-id="5ba80-126">The lower the quality, the faster the object prints.</span></span> <span data-ttu-id="5ba80-127"><strong>Haute</strong> est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5ba80-127">The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba80-128"><strong>Copies</strong></span><span class="sxs-lookup"><span data-stu-id="5ba80-128"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba80-129">Nombre de copies à imprimer.</span><span class="sxs-lookup"><span data-stu-id="5ba80-129">The number of copies to print.</span></span> <span data-ttu-id="5ba80-130">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="5ba80-130">The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba80-131"><strong>Copies triées</strong></span><span class="sxs-lookup"><span data-stu-id="5ba80-131"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba80-p107">Cliquez sur <strong>Oui</strong> (les copies imprimées sont triées) ou <strong>Non</strong> (elles ne sont pas triées). L’impression de l’objet peut être plus rapide si cet argument a la valeur <strong>Non</strong>. La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="5ba80-p107">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5ba80-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ba80-135">Remarks</span></span>

<span data-ttu-id="5ba80-p108">Cette action équivaut à sélectionner un objet, à cliquer sur l'onglet **Fichier**, puis à cliquer sur **Imprimer**. Toutefois, avec cette action, aucune boîte de dialogue **Imprimer** ne s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="5ba80-p108">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**. With this action, however, no **Print** dialog box appears.</span></span>

> [!TIP]
> <span data-ttu-id="5ba80-138">[!CONSEIL] Si vous utilisez fréquemment des paramètres d'impression spécifiques, créez une macro contenant une action **Imprimer** reprenant ces paramètres dans ses arguments.</span><span class="sxs-lookup"><span data-stu-id="5ba80-138">If you have particular print settings you use frequently, create a macro containing a **PrintOut** action with these settings in its arguments.</span></span>

<span data-ttu-id="5ba80-p109">Les arguments à spécifier pour cette action correspondent aux options de la boîte de dialogue **Imprimer**. Toutefois, à la différence de l'action **TrouverEnregistrement** et la boîte de dialogue **Rechercher et remplacer**, les paramètres des arguments ne sont pas partagés avec les options de la boîte de dialogue **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="5ba80-p109">The arguments for this action correspond to options in the **Print** dialog box. However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="5ba80-141">Pour exécuter l'action **Imprimer** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **PrintOut** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="5ba80-141">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

