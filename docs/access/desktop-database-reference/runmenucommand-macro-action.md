---
title: ExécuterCommandeMenu, action de macro
TOCTitle: RunMenuCommand Macro Action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 372803779767ea6fdc12b4e10b5dde231ce101fc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875511"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="de750-102">ExécuterCommandeMenu, action de macro</span><span class="sxs-lookup"><span data-stu-id="de750-102">RunMenuCommand Macro Action</span></span>


<span data-ttu-id="de750-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de750-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de750-104">Vous pouvez utiliser l'action **ExécuterCommandeMenu** pour exécuter une commande Microsoft Office Access.</span><span class="sxs-lookup"><span data-stu-id="de750-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="de750-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="de750-105">Setting</span></span>

<span data-ttu-id="de750-106">L'action **ExécuterCommandeMenu** utilise l'argument d'action suivant :</span><span class="sxs-lookup"><span data-stu-id="de750-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de750-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="de750-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="de750-108">Description</span><span class="sxs-lookup"><span data-stu-id="de750-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de750-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="de750-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="de750-p101">Nom de la commande à exécuter. La zone <strong>Commande</strong> affiche les commandes intégrées disponibles dans Access et classées par ordre alphabétique. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="de750-p101">The name of the command you want to run. The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="de750-113">Notes</span><span class="sxs-lookup"><span data-stu-id="de750-113">Remarks</span></span>

<span data-ttu-id="de750-114">Vous pouvez utiliser l'action **ExécuterCommandeMenu** pour exécuter une commande Access à partir d'une barre de menus personnalisée, d'une barre de menus globale, d'un menu contextuel personnalisé ou d'un menu contextuel global.</span><span class="sxs-lookup"><span data-stu-id="de750-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="de750-115">Vous pouvez utiliser l'action **ExécuterCommandeMenu** dans une macro avec des expressions conditionnelles pour exécuter une commande en fonction de certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="de750-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>


> [!NOTE]
> <P><span data-ttu-id="de750-p102">[!REMARQUE] Si vous cliquez sur l'onglet <STRONG>Fichier</STRONG>, puis sur <STRONG>Récent</STRONG>, les bases de données récemment utilisées s'affichent. Vous pouvez cliquer sur l'une de ces bases de données au lieu de cliquer sur <STRONG>Ouvrir</STRONG>. Ces éléments de base de données ne s'affichent pas dans la zone de liste déroulante de l'argument <STRONG>Commande</STRONG> et ne sont pas disponibles lorsque vous utilisez l'action <STRONG>ExécuterCommandeMenu</STRONG> dans une macro.</span><span class="sxs-lookup"><span data-stu-id="de750-p102">Clicking the <STRONG>File</STRONG> tab and then clicking <STRONG>Recent</STRONG> shows the most recently used databases. You can click one of these databases instead of clicking <STRONG>Open</STRONG>. These database items don't appear in the drop-down list box for the <STRONG>Command</STRONG> argument, and aren't available by using the <STRONG>RunMenuCommand</STRONG> action in a macro.</span></span></P>



<span data-ttu-id="de750-p103">Il se peut que certaines commandes ne soient plus disponibles lorsque vous convertissez une base de données créée avec une version précédente d'Access. Une commande peut avoir été renommée, transférée vers un autre menu ou n'existe peut-être plus dans Access. Les actions **ExécuterElémentMenu** pour de telles commandes ne peuvent pas être converties en actions **ExécuterCommandeMenu**. Lorsque vous ouvrez la macro, Access affichera une action **ExécuterCommandeMenu** avec un argument **Commande** vide pour ces commandes. Vous devez modifier la macro et entrer un argument Commande valide ou supprimer l'action **ExécuterCommandeMenu**.</span><span class="sxs-lookup"><span data-stu-id="de750-p103">When you convert an Access database from a previous version of Access, some commands may no longer be available. A command may have been renamed, moved to a different menu, or may no longer be available in Access. The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions. When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands. You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="de750-p104">Pour exécuter l'action **ExécuterCommandeMenu** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **RunCommand** de l'objet **Application**. (Elle correspond à la méthode **RunCommand** de l'objet **DoCmd**.)</span><span class="sxs-lookup"><span data-stu-id="de750-p104">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object. (This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

