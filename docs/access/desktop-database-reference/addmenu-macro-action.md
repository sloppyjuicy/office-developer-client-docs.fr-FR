---
title: AjouterMenu, action de macro
TOCTitle: AddMenu Macro Action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 984b10638ab7f01aeb4dc9656bc70aa1e44d56a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471392"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="15989-102">AjouterMenu, action de macro</span><span class="sxs-lookup"><span data-stu-id="15989-102">AddMenu Macro Action</span></span>


<span data-ttu-id="15989-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="15989-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="15989-104">Cet article décrit le fonctionnement de base de l'action de macro **AjouterMenu**.</span><span class="sxs-lookup"><span data-stu-id="15989-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="15989-105">Vous pouvez utiliser l'action **AjouterMenu** pour créer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="15989-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="15989-106">des menus personnalisés sous l'onglet **Compléments** d'un formulaire ou d'un état particulier ;</span><span class="sxs-lookup"><span data-stu-id="15989-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="15989-p101">un menu contextuel personnalisé pour un formulaire, un état ou un contrôle. Le menu contextuel personnalisé remplace le menu contextuel intégré pour le formulaire, l'état ou le contrôle ;</span><span class="sxs-lookup"><span data-stu-id="15989-p101">A custom shortcut menu for a form, report, or control. The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="15989-p102">un menu contextuel global. Le menu contextuel global remplace le menu contextuel intégré pour les champs des feuilles de données de table et de requête, des formulaires et des états, sauf là où vous avez ajouté un menu contextuel personnalisé pour un formulaire, un état ou un contrôle.</span><span class="sxs-lookup"><span data-stu-id="15989-p102">A global shortcut menu. The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="15989-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="15989-111">Setting</span></span>

<span data-ttu-id="15989-112">L'action **AjouterMenu** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="15989-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15989-113">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="15989-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="15989-114">Description</span><span class="sxs-lookup"><span data-stu-id="15989-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15989-115"><strong>Nom du menu</strong></span><span class="sxs-lookup"><span data-stu-id="15989-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="15989-116">Le nom du menu, par exemple, &quot;rapport commandes&quot; ou &quot;outils&quot;.</span><span class="sxs-lookup"><span data-stu-id="15989-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="15989-117">Pour créer une touche d’accès afin que vous puissiez utiliser le clavier pour choisir le menu, tapez un « et commercial » (<strong>&amp;</strong>) avant la lettre que vous voulez être la touche d’accès.</span><span class="sxs-lookup"><span data-stu-id="15989-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="15989-118">Cette lettre sera soulignée dans le nom du menu dans l’onglet <strong>Compléments</strong> .</span><span class="sxs-lookup"><span data-stu-id="15989-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15989-119"><strong>Nom de la macro de menu</strong></span><span class="sxs-lookup"><span data-stu-id="15989-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="15989-p104">Nom du groupe de macros qui contient les macros pour les commandes du menu. Cet argument est obligatoire. 

</span><span class="sxs-lookup"><span data-stu-id="15989-p104">The name of the macro group that contains the macros for the menu's commands. This is a required argument.</span></span></p>

> [!NOTE]
> <span data-ttu-id="15989-122">Si vous exécutez une macro contenant l’action **AjouterMenu** dans une base de données bibliothèque, Microsoft Office Access 2007 recherche le groupe de macros portant ce nom uniquement dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="15989-122">If you run a macro containing the **AddMenu** action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15989-123"><strong>Texte de la barre d’état</strong></span><span class="sxs-lookup"><span data-stu-id="15989-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="15989-p105">Texte à afficher dans la barre d’état lorsque le menu est sélectionné. Cet argument est ignoré pour les menus contextuels</span><span class="sxs-lookup"><span data-stu-id="15989-p105">The text to display in the status bar when the menu is selected. This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="15989-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="15989-126">Remarks</span></span>

<span data-ttu-id="15989-p106">Pour exécuter l'action **AjouterMenu** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **AddMenu** de l'objet **DoCmd**. Vous pouvez également définir la propriété **MenuBar** ou **ShortcutMenuBar** dans VBA pour créer un menu contextuel sous l'onglet **Compléments** ou pour attacher un menu contextuel personnalisé à un formulaire, un rapport ou un contrôle. Vous pouvez définir la propriété **ShortcutMenuBar** de l'objet **Application** pour créer un menu contextuel global.</span><span class="sxs-lookup"><span data-stu-id="15989-p106">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object. You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control. You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

