---
title: ShowToolbar, action de macro
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 01ba59ce0898068788adb9269b3203794d1f31d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306474"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="b47c1-102">ShowToolbar, action de macro</span><span class="sxs-lookup"><span data-stu-id="b47c1-102">ShowToolbar macro action</span></span>

<span data-ttu-id="b47c1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b47c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b47c1-104">L'action **AfficherBarreOutils** permet d'afficher ou de masquer un groupe de commandes sous l'onglet **Compléments**.</span><span class="sxs-lookup"><span data-stu-id="b47c1-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="b47c1-105">[!REMARQUE] L'action **AfficherBarreOutils** n'affecte pas les menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="b47c1-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="b47c1-106">Cette action ne sera pas autorisée si la base de données n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="b47c1-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="b47c1-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b47c1-107">Setting</span></span>

<span data-ttu-id="b47c1-108">L’action **AfficherBarreOutils** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b47c1-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b47c1-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="b47c1-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b47c1-110">Description</span><span class="sxs-lookup"><span data-stu-id="b47c1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b47c1-111"><strong>Nom de la barre d’outils</strong></span><span class="sxs-lookup"><span data-stu-id="b47c1-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b47c1-112">Nom du groupe de commandes de l’onglet <strong>Compléments</strong> que vous souhaitez afficher ou masquer.</span><span class="sxs-lookup"><span data-stu-id="b47c1-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="b47c1-113">Le champ <strong>Nom de la barre d’outils</strong> de la section <strong>Arguments de l’action</strong> du Générateur de macro présente tous les groupes disponibles pouvant être affectés par cette action.</span><span class="sxs-lookup"><span data-stu-id="b47c1-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="b47c1-114">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b47c1-114">This is a required argument.</span></span> <span data-ttu-id="b47c1-115">Si vous exécutez une macro contenant l’action <strong>AfficherBarreOutils</strong> dans une base de données bibliothèque, Access recherche un groupe portant ce nom, d’abord dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="b47c1-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b47c1-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="b47c1-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="b47c1-117">Indique si le groupe doit être affiché ou masqué, et dans quel mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b47c1-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="b47c1-118">La valeur par défaut est <strong>Oui</strong> (afficher le groupe en permanence).</span><span class="sxs-lookup"><span data-stu-id="b47c1-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="b47c1-119">Vous pouvez sélectionner <strong>Oui</strong> pour afficher le groupe en permanence, le <strong>cas échéant</strong> pour afficher le groupe uniquement lorsque le formulaire ou l'état approprié est actif, ou <strong>non</strong> pour masquer le groupe en permanence.</span><span class="sxs-lookup"><span data-stu-id="b47c1-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b47c1-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="b47c1-120">Remarks</span></span>

<span data-ttu-id="b47c1-121">Utilisez cette action dans une macro avec des expressions conditionnelles pour afficher ou masquer un groupe sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="b47c1-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="b47c1-p103">Si vous voulez afficher un groupe spécifique dans un seul formulaire ou état, vous pouvez définir la propriété **SurActivé** de ce formulaire ou état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour afficher le groupe. Définissez ensuite la propriété **SurDésactivé** du formulaire ou de l'état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour masquer le groupe.</span><span class="sxs-lookup"><span data-stu-id="b47c1-p103">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="b47c1-124">Les barres d'outils prédéfinies ne permettent ni d'afficher, ni de masquer des éléments via cette action si vous avez défini la propriété **AllowBuiltInToolbars** sur **False** (0) dans un module Visual Basic pour Applications (VBA), ou si vous avez défini l'option **Afficher les barres d'outils intégrées** sur **False** dans VBA, via la méthode **SetOption**.</span><span class="sxs-lookup"><span data-stu-id="b47c1-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="b47c1-125">Pour exécuter l'action **AfficherBarreOutils** dans un module VBA, utilisez la méthode **ShowToolbar** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="b47c1-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

