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
ms.openlocfilehash: 254a54b4b672ba9e40253e3bd95283eec655d3dc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920507"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="c1f22-102">ShowToolbar, action de macro</span><span class="sxs-lookup"><span data-stu-id="c1f22-102">ShowToolbar macro action</span></span>


<span data-ttu-id="c1f22-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1f22-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1f22-104">L'action **AfficherBarreOutils** permet d'afficher ou de masquer un groupe de commandes sous l'onglet **Compléments**.</span><span class="sxs-lookup"><span data-stu-id="c1f22-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c1f22-105">[!REMARQUE] L'action <STRONG>AfficherBarreOutils</STRONG> n'affecte pas les menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="c1f22-105">The <STRONG>ShowToolbar</STRONG> action does not affect shortcut menus.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="c1f22-p101">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="c1f22-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="c1f22-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1f22-108">Setting</span></span>

<span data-ttu-id="c1f22-109">L'action **AfficherBarreOutils** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c1f22-109">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1f22-110">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="c1f22-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c1f22-111">Description</span><span class="sxs-lookup"><span data-stu-id="c1f22-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1f22-112"><strong>Nom de la barre d’outils</strong></span><span class="sxs-lookup"><span data-stu-id="c1f22-112"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c1f22-113">Le nom du groupe de commandes sous l’onglet <strong>Compléments</strong> que vous souhaitez afficher ou masquer.</span><span class="sxs-lookup"><span data-stu-id="c1f22-113">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="c1f22-114">La zone <strong>Nom de la barre d’outils</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro affiche tous les groupes disponibles qui peuvent être affectées par cette action.</span><span class="sxs-lookup"><span data-stu-id="c1f22-114">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="c1f22-115">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c1f22-115">This is a required argument.</span></span> <span data-ttu-id="c1f22-116">Si vous exécutez une macro contenant l’action <strong>AfficherBarreOutils</strong> dans une base de données bibliothèque, Access recherche un groupe portant ce nom, d’abord dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="c1f22-116">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1f22-117"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="c1f22-117"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="c1f22-118">Spécifie s’il faut afficher ou masquer le groupe et dans les modes d’affichage pour afficher ou masquer.</span><span class="sxs-lookup"><span data-stu-id="c1f22-118">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="c1f22-119">La valeur par défaut est <strong>Oui</strong> (afficher le groupe en permanence).</span><span class="sxs-lookup"><span data-stu-id="c1f22-119">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="c1f22-120">Vous pouvez sélectionner <strong>Oui</strong> pour afficher le groupe à toutes les heures <strong>Où approprié</strong> pour afficher le groupe uniquement lorsque le formulaire adéquat ou l’état est actif, ou <strong>non</strong> pour masquer le groupe en permanence.</span><span class="sxs-lookup"><span data-stu-id="c1f22-120">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c1f22-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1f22-121">Remarks</span></span>

<span data-ttu-id="c1f22-122">Utilisez cette action dans une macro avec des expressions conditionnelles pour afficher ou masquer un groupe sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="c1f22-122">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="c1f22-p104">Si vous voulez afficher un groupe spécifique dans un seul formulaire ou état, vous pouvez définir la propriété **SurActivé** de ce formulaire ou état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour afficher le groupe. Définissez ensuite la propriété **SurDésactivé** du formulaire ou de l'état sur le nom d'une macro contenant une action **AfficherBarreOutils** pour masquer le groupe.</span><span class="sxs-lookup"><span data-stu-id="c1f22-p104">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="c1f22-125">Les barres d'outils prédéfinies ne permettent ni d'afficher, ni de masquer des éléments via cette action si vous avez défini la propriété **AllowBuiltInToolbars** sur **False** (0) dans un module Visual Basic pour Applications (VBA), ou si vous avez défini l'option **Afficher les barres d'outils intégrées** sur **False** dans VBA, via la méthode **SetOption**.</span><span class="sxs-lookup"><span data-stu-id="c1f22-125">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="c1f22-126">Pour exécuter l'action **AfficherBarreOutils** dans un module VBA, utilisez la méthode **ShowToolbar** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="c1f22-126">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

