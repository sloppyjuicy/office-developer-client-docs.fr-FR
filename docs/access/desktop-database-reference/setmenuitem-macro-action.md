---
title: SetMenuItem, action de macro
TOCTitle: SetMenuItem macro action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fe61a3368813ba3420920909f818beee2029d993
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709424"
---
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="88c2e-102">SetMenuItem, action de macro</span><span class="sxs-lookup"><span data-stu-id="88c2e-102">SetMenuItem macro action</span></span>

<span data-ttu-id="88c2e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88c2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88c2e-104">Vous pouvez utiliser l'action **DéfinirElémentMenu** pour définir l'état des éléments de menu (activé, désactivé, sélectionné ou non sélectionné) dans les menus globaux ou personnalisés de l'onglet **Compléments**.</span><span class="sxs-lookup"><span data-stu-id="88c2e-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="88c2e-p101">[!REMARQUE] L'action **DéfinirElémentMenu** fonctionne uniquement avec les menus personnalisés et globaux générés à l'aide de macros de menu. L'action **DéfinirElémentMenu** est incluse dans Microsoft Access à la seule fin de compatibilité avec les versions antérieures. Il ne fonctionne pas avec les fonctionnalités de la barre de commandes. Vous pouvez toutefois utiliser les propriétés **Enabled** et **State** dans un module Visual Basic pour Applications (VBA) afin de désactiver, d'activer, de sélectionner ou de désélectionner des éléments des menus contextuels ou des menus personnalisés ou globaux.</span><span class="sxs-lookup"><span data-stu-id="88c2e-p101">The **SetMenuItem** action works only with custom and global menus created by using menu macros. The **SetMenuItem** action is included in Microsoft Access only for compatibility with previous versions. It does not work with the command bar functionality. However, you can use the **Enabled** and **State** properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span>

## <a name="setting"></a><span data-ttu-id="88c2e-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="88c2e-109">Setting</span></span>

<span data-ttu-id="88c2e-110">L'action **DéfinirElémentMenu** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="88c2e-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88c2e-111">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="88c2e-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="88c2e-112">Description</span><span class="sxs-lookup"><span data-stu-id="88c2e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88c2e-113"><strong>Index de menu</strong></span><span class="sxs-lookup"><span data-stu-id="88c2e-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="88c2e-114">L’index du menu qui contient la commande pour laquelle vous souhaitez définir l’état.</span><span class="sxs-lookup"><span data-stu-id="88c2e-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="88c2e-115">Entrez une valeur entière, à partir de 0, pour l’index du menu souhaité dans le menu personnalisé ou global.</span><span class="sxs-lookup"><span data-stu-id="88c2e-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="88c2e-116">Dans la zone <strong>Index de Menu</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro, entrez la valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="88c2e-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="88c2e-117">L’index est par rapport à la position du menu dans la macro de menu pour le menu personnalisé ou global (position de l’action <strong>AjouterMenu</strong> de ce menu dans la macro de menu, à partir de 0).</span><span class="sxs-lookup"><span data-stu-id="88c2e-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="88c2e-118">L’affichage du menu peut être légèrement différent, car vous pouvez utiliser des expressions conditionnelles dans la macro de menu pour masquer ou afficher des éléments de menu personnalisés.</span><span class="sxs-lookup"><span data-stu-id="88c2e-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="88c2e-119">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="88c2e-119">This is a required argument.</span></span> <span data-ttu-id="88c2e-120">Si vous sélectionnez un menu avec cet argument et laissez les arguments <strong>Index de commande</strong> et <strong>Index de sous-commande</strong> vides, vous pouvez activer ou désactiver le nom du menu lui-même.</span><span class="sxs-lookup"><span data-stu-id="88c2e-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="88c2e-121">Toutefois, vous ne peut pas sélectionner ou désélectionner un nom de menu (Access ignore les paramètres <strong>coché</strong> et <strong>non coché</strong> de l’argument <strong>indicateur</strong> pour les noms de menu).</span><span class="sxs-lookup"><span data-stu-id="88c2e-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88c2e-122"><strong>Index de commande</strong></span><span class="sxs-lookup"><span data-stu-id="88c2e-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="88c2e-p103">Index de la commande dont vous souhaitez définir l’état. Entrez une valeur entière, à partir de 0, pour l’index de la commande souhaitée dans le menu sélectionné par l’argument <strong>Index de menu</strong>. L’index est relatif à la position de la commande dans le groupe de macros qui définit le menu sélectionné pour le menu personnalisé ou global (position de la macro de cette commande dans le groupe de macros, à partir de 0). L’affichage du menu peut être légèrement différent dans la mesure où vous pouvez utiliser des expressions conditionnelles dans le groupe de macros du menu pour masquer ou afficher les commandes de menu personnalisées.</span><span class="sxs-lookup"><span data-stu-id="88c2e-p103">The index of the command for which you want to set the state. Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument. The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0). The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88c2e-127"><strong>Index de sous-commande</strong></span><span class="sxs-lookup"><span data-stu-id="88c2e-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="88c2e-p104">Index de la sous-commande dont vous souhaitez définir l’état. Cet argument n’est applicable qu’à partir du moment où la commande souhaitée possède un sous-menu. Entrez une valeur entière, à partir de 0, pour l’index de la sous-commande requise dans le sous-menu sélectionné par l’argument <strong>Index de commande</strong>. L’index est relatif à la position de la sous-commande dans le groupe de macros qui définit le sous-menu sélectionné pour le menu personnalisé ou global (position de la macro de cette sous-commande dans le groupe de macros, à partir de 0).</span><span class="sxs-lookup"><span data-stu-id="88c2e-p104">The index of the subcommand for which you want to set the state. This applies only if the desired command has a submenu. Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument. The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88c2e-132"><strong>Flag</strong></span><span class="sxs-lookup"><span data-stu-id="88c2e-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="88c2e-p105">État à affecter à la commande ou à la sous-commande. Cliquez sur <strong>Grisé</strong> (pour désactiver la commande qui apparaît estompée), <strong>Non grisé</strong> (pour l’activer), <strong>Coché</strong> (pour placer une coche en regard de la commande, ce qui indique en général qu’elle a été sélectionnée) ou <strong>Non coché</strong> (pour supprimer la coche). La valeur par défaut est <strong>Non grisé</strong>.</span><span class="sxs-lookup"><span data-stu-id="88c2e-p105">The state you want to set the command or subcommand to. Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check). The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="88c2e-136">Notes</span><span class="sxs-lookup"><span data-stu-id="88c2e-136">Remarks</span></span>

<span data-ttu-id="88c2e-p106">L'action **DéfinirElémentMenu** fonctionne uniquement avec un menu personnalisé ou global. Si la fenêtre active ne possède pas de menu personnalisé ou global, l'exécution d'une macro contenant l'action **DéfinirElémentMenu** provoque une erreur d'exécution.</span><span class="sxs-lookup"><span data-stu-id="88c2e-p106">The **SetMenuItem** action works only on a custom or global menu. If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="88c2e-139">Vous pouvez utiliser cette action pour définir l'état des commandes et sous-commandes de menu, mais non des sous-commandes de sous-commandes.</span><span class="sxs-lookup"><span data-stu-id="88c2e-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="88c2e-140">Pour exécuter l'action **DéfinirÉlémentMenu** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SetMenuItem** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="88c2e-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

