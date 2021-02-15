---
title: OpenStoredProcedure, action de macro
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b972174e4fe7f3c0384b7483e17eb5ceb9e8bc15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288307"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="0753e-102">OpenStoredProcedure, action de macro</span><span class="sxs-lookup"><span data-stu-id="0753e-102">OpenStoredProcedure macro action</span></span>

<span data-ttu-id="0753e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0753e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0753e-p101">Dans un projet Access, vous pouvez utiliser l’action **OuvrirProcédureStockée** pour ouvrir une procédure stockée en mode Feuille de données, Création de procédure stockée ou Aperçu avant impression. Cette action exécute la procédure stockée nommée lorsqu’elle est ouverte en mode Feuille de données. Vous pouvez choisir le mode de saisie des données voulu pour la procédure stockée et limiter les enregistrements que celle-ci affiche.</span><span class="sxs-lookup"><span data-stu-id="0753e-p101">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview. This action runs the named stored procedure when opened in Datasheet view. You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>

> [!NOTE]
> <span data-ttu-id="0753e-107">Cette action ne sera pas autorisée si la base de données n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="0753e-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="0753e-108">Setting</span><span class="sxs-lookup"><span data-stu-id="0753e-108">Setting</span></span>

<span data-ttu-id="0753e-109">L’action **OuvrirProcédureStockée** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="0753e-109">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0753e-110">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="0753e-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0753e-111">Description</span><span class="sxs-lookup"><span data-stu-id="0753e-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0753e-112"><strong>Nom de la procédure</strong></span><span class="sxs-lookup"><span data-stu-id="0753e-112"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0753e-113">Nom de la procédure stockée à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="0753e-113">The name of the stored procedure to open.</span></span> <span data-ttu-id="0753e-114">La <strong>zone Nom de</strong> la procédure de la section Arguments de l’action du volet Générateur de macro affiche toutes les procédures stockées dans la base de données actuelle. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="0753e-114">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="0753e-115">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0753e-115">This is a required argument.</span></span> <span data-ttu-id="0753e-116">Si vous exécutez une macro contenant l’action <strong>OuvrirProcédureStockée</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord la procédure stockée portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="0753e-116">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0753e-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="0753e-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="0753e-p103">Affichage dans lequel s’ouvre la procédure stockée. Cliquez sur <strong>Feuille de données</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Feuille de données</strong>.</span><span class="sxs-lookup"><span data-stu-id="0753e-p103">The view in which the stored procedure will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0753e-121"><strong>Mode Données</strong></span><span class="sxs-lookup"><span data-stu-id="0753e-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="0753e-p104">Mode de saisie de données de la procédure stockée. S’applique uniquement aux procédures stockées ouvertes en mode Feuille de données. Cliquez sur <strong>Ajouter</strong> (l’utilisateur ne peut ni afficher ni modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l’utilisateur peut afficher et modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> (l’utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>.</span><span class="sxs-lookup"><span data-stu-id="0753e-p104">The data entry mode for the stored procedure. This applies only to stored procedures opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="0753e-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="0753e-126">Remarks</span></span>

<span data-ttu-id="0753e-127">Cette action équivaut à double-cliquer sur la procédure stockée dans le volet de navigation ou à cliquer avec le bouton droit sur la procédure stockée dans le volet de navigation, puis à sélectionner la commande de votre choix.</span><span class="sxs-lookup"><span data-stu-id="0753e-127">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="0753e-p105">Basculer en mode Création lorsque la procédure stockée est ouverte supprime le paramètre de l’argument **Mode Données** de la procédure stockée. Ce paramètre n’est pas actif, même si l’utilisateur revient en mode Feuille de données.</span><span class="sxs-lookup"><span data-stu-id="0753e-p105">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="0753e-130">Vous pouvez faire glisser une procédure stockée du volet de navigation vers une ligne d’action de macro.</span><span class="sxs-lookup"><span data-stu-id="0753e-130">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="0753e-131">Ceci crée automatiquement une action **OuvrirProcédureStockée** qui ouvre la procédure stockée en mode Feuille de données.</span><span class="sxs-lookup"><span data-stu-id="0753e-131">This automatically creates an **OpenStoredProcedure** action that opens the stored procedure in Datasheet view.</span></span>
> - <span data-ttu-id="0753e-132">Si vous ne voulez pas afficher les messages système qui s’affichent normalement lorsqu’une procédure stockée est exécutée (indiquant qu’il s’agit d’une procédure stockée et affichant le nombre d’enregistrements concernés), vous pouvez faire appel à l’action **Avertissements** pour supprimer l’affichage de ces messages.</span><span class="sxs-lookup"><span data-stu-id="0753e-132">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="0753e-133">Pour exécuter l’action **OuvrirProcédureStockée** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenStoredProcedure** de l’objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="0753e-133">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

