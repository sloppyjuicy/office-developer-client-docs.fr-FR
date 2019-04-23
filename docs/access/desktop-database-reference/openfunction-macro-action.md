---
title: OpenFunction, action de macro
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b13d21ef1bd8a95587eb78cd448f19f9fd0c24c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288363"
---
# <a name="openfunction-macro-action"></a><span data-ttu-id="d7347-102">OpenFunction, action de macro</span><span class="sxs-lookup"><span data-stu-id="d7347-102">OpenFunction macro action</span></span>

<span data-ttu-id="d7347-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7347-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7347-p101">Dans un projet Access, vous pouvez utiliser l'action **OuvrirFonction** pour ouvrir une fonction définie par l'utilisateur en mode Feuille de données, une fonction en ligne en mode Création, l'Éditeur de texte SQL (pour une fonction scalaire ou une fonction tabulaire définie par l'utilisateur) ou un Aperçu avant impression. Cette action exécute la fonction définie par l'utilisateur lorsqu'elle est ouverte en mode Feuille de données. Vous pouvez également sélectionner le mode de saisie de données pour la fonction définie par l'utilisateur et limiter les enregistrements que celle-ci affiche.</span><span class="sxs-lookup"><span data-stu-id="d7347-p101">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview. This action runs the user-defined function when opened in Datasheet view. You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>

> [!NOTE]
> <span data-ttu-id="d7347-107">Cette action ne sera pas autorisée si la base de données n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="d7347-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="d7347-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d7347-108">Setting</span></span>

<span data-ttu-id="d7347-109">L’action **OuvrirFonction** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="d7347-109">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7347-110">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="d7347-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d7347-111">Description</span><span class="sxs-lookup"><span data-stu-id="d7347-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7347-112"><strong>Nom de la fonction</strong></span><span class="sxs-lookup"><span data-stu-id="d7347-112"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d7347-113">Nom de la fonction définie par l’utilisateur à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="d7347-113">The name of the user-defined function to open.</span></span> <span data-ttu-id="d7347-114">La zone <strong>Nom de la fonction</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro affiche toutes les fonctions définies par l’utilisateur dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="d7347-114">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="d7347-115">Il s'agit d'un argument obligatoire. Si vous exécutez une macro contenant l'action <strong>fonction</strong> dans une base de données bibliothèque, Microsoft Access recherche d'abord la fonction portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="d7347-115">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7347-116"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="d7347-116"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="d7347-p103">Affichage dans lequel s’ouvre la fonction définie par l’utilisateur. Cliquez sur <strong>Feuille de données</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Feuille de données</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7347-p103">The view in which the user-defined function will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7347-120"><strong>Mode Données</strong></span><span class="sxs-lookup"><span data-stu-id="d7347-120"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="d7347-p104">Mode de saisie de données de la fonction définie par l’utilisateur. S’applique uniquement aux fonctions définies par l’utilisateur ouvertes en mode Feuille de données. Cliquez sur <strong>Ajouter</strong> (l’utilisateur ne peut ni afficher ni modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l’utilisateur peut afficher et modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> (l’utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7347-p104">The data entry mode for the user-defined function. This applies only to user-defined functions opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d7347-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7347-125">Remarks</span></span>

<span data-ttu-id="d7347-126">Cette action équivaut à double-cliquer sur une fonction définie par l’utilisateur dans le volet de navigation ou à cliquer avec le bouton droit sur la fonction dans le volet de navigation et à choisir un affichage.</span><span class="sxs-lookup"><span data-stu-id="d7347-126">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="d7347-p105">Basculer en mode Création lorsque la fonction définie par l'utilisateur est ouverte supprime le paramètre de l'argument **Mode Données** de la fonction. Ce paramètre n'est pas actif, même si l'utilisateur revient en mode Feuille de données.</span><span class="sxs-lookup"><span data-stu-id="d7347-p105">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="d7347-p106">Vous pouvez sélectionner une fonction définie par l'utilisateur dans le volet de navigation et la faire glisser vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirFonction** qui ouvre la fonction définie par l'utilisateur en mode Feuille de données.</span><span class="sxs-lookup"><span data-stu-id="d7347-p106">You can select a user-defined function in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>
> - <span data-ttu-id="d7347-131">Si vous ne voulez pas afficher les messages système qui s'affichent normalement lorsqu'une fonction définie par l'utilisateur est exécutée (indiquant qu'il s'agit d'une fonction définie par l'utilisateur et affichant le nombre d'enregistrements concernés), vous pouvez faire appel à l'action **Avertissements** pour supprimer l'affichage de ces messages.</span><span class="sxs-lookup"><span data-stu-id="d7347-131">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="d7347-132">Pour exécuter l'action **OuvrirFonction** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenFunction** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d7347-132">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

