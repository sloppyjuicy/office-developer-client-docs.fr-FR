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
ms.openlocfilehash: ed69a84f9b1774b7c33711a0bb8e80da54e656cc
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997929"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="b829f-102">ShowToolbar, action de macro</span><span class="sxs-lookup"><span data-stu-id="b829f-102">ShowToolbar macro action</span></span>

<span data-ttu-id="b829f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b829f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b829f-104">L'action **AfficherBarreOutils** permet d'afficher ou de masquer un groupe de commandes sous l'onglet **Compléments**.</span><span class="sxs-lookup"><span data-stu-id="b829f-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="b829f-105">[!REMARQUE] L'action **AfficherBarreOutils** n'affecte pas les menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="b829f-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="b829f-106">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="b829f-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="b829f-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="b829f-107">Setting</span></span>

<span data-ttu-id="b829f-108">L'action **AfficherBarreOutils** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b829f-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b829f-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="b829f-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b829f-110">Description</span><span class="sxs-lookup"><span data-stu-id="b829f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b829f-111"><strong>Nom de la barre d’outils</strong></span><span class="sxs-lookup"><span data-stu-id="b829f-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b829f-112">Le nom du groupe de commandes sous l’onglet <strong>Compléments</strong> que vous souhaitez afficher ou masquer.</span><span class="sxs-lookup"><span data-stu-id="b829f-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="b829f-113">La zone <strong>Nom de la barre d’outils</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro affiche tous les groupes disponibles qui peuvent être affectées par cette action.</span><span class="sxs-lookup"><span data-stu-id="b829f-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="b829f-114">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b829f-114">This is a required argument.</span></span> <span data-ttu-id="b829f-115">Si vous exécutez une macro contenant l’action <strong>AfficherBarreOutils</strong> dans une base de données bibliothèque, Access recherche un groupe portant ce nom, d’abord dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="b829f-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b829f-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="b829f-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="b829f-117">Spécifie s’il faut afficher ou masquer le groupe et dans les modes d’affichage pour afficher ou masquer.</span><span class="sxs-lookup"><span data-stu-id="b829f-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="b829f-118">La valeur par défaut est <strong>Oui</strong> (afficher le groupe en permanence).</span><span class="sxs-lookup"><span data-stu-id="b829f-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="b829f-119">Vous pouvez sélectionner <strong>Oui</strong> pour afficher le groupe à toutes les heures <strong>Où approprié</strong> pour afficher le groupe uniquement lorsque le formulaire adéquat ou l’état est actif, ou <strong>non</strong> pour masquer le groupe en permanence.</span><span class="sxs-lookup"><span data-stu-id="b829f-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b829f-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="b829f-120">Remarks</span></span>

<span data-ttu-id="b829f-121">Utilisez cette action dans une macro avec des expressions conditionnelles pour afficher ou masquer un groupe sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="b829f-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="b829f-p103">Si vous voulez afficher un groupe spécifique dans un seul formulaire ou état, vous pouvez définir la propriété **SurActivé** de ce formulaire ou état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour afficher le groupe. Définissez ensuite la propriété **SurDésactivé** du formulaire ou de l'état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour masquer le groupe.</span><span class="sxs-lookup"><span data-stu-id="b829f-p103">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="b829f-124">Les barres d'outils prédéfinies ne permettent ni d'afficher, ni de masquer des éléments via cette action si vous avez défini la propriété **AllowBuiltInToolbars** sur **False** (0) dans un module Visual Basic pour Applications (VBA), ou si vous avez défini l'option **Afficher les barres d'outils intégrées** sur **False** dans VBA, via la méthode **SetOption**.</span><span class="sxs-lookup"><span data-stu-id="b829f-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="b829f-125">Pour exécuter l'action **AfficherBarreOutils** dans un module VBA, utilisez la méthode **ShowToolbar** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="b829f-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

