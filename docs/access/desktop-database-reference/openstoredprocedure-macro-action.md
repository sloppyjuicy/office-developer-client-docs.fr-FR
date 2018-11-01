---
title: OuvrirProcédureStockée, action de macro
TOCTitle: OpenStoredProcedure Macro Action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 52d7d6c54913511ab593ee77d374ed55984ed40b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883252"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="12d00-102">OuvrirProcédureStockée, action de macro</span><span class="sxs-lookup"><span data-stu-id="12d00-102">OpenStoredProcedure Macro Action</span></span>


<span data-ttu-id="12d00-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12d00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12d00-p101">Dans un projet Access, vous pouvez utiliser l’action **OuvrirProcédureStockée** pour ouvrir une procédure stockée en mode Feuille de données, Création de procédure stockée ou Aperçu avant impression. Cette action exécute la procédure stockée nommée lorsqu’elle est ouverte en mode Feuille de données. Vous pouvez choisir le mode de saisie des données voulu pour la procédure stockée et limiter les enregistrements que celle-ci affiche.</span><span class="sxs-lookup"><span data-stu-id="12d00-p101">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview. This action runs the named stored procedure when opened in Datasheet view. You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="12d00-p102">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="12d00-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="12d00-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="12d00-109">Setting</span></span>

<span data-ttu-id="12d00-110">L’action **OuvrirProcédureStockée** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="12d00-110">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12d00-111">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="12d00-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="12d00-112">Description</span><span class="sxs-lookup"><span data-stu-id="12d00-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12d00-113"><strong>Nom de la procédure</strong></span><span class="sxs-lookup"><span data-stu-id="12d00-113"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="12d00-114">Nom de la procédure stockée à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="12d00-114">The name of the stored procedure to open.</span></span> <span data-ttu-id="12d00-115">La zone <strong>Nom procédure dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro</strong> affiche toutes les procédures stockées dans la base de données en cours.</span><span class="sxs-lookup"><span data-stu-id="12d00-115">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="12d00-116">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="12d00-116">This is a required argument.</span></span> <span data-ttu-id="12d00-117">Si vous exécutez une macro contenant l’action <strong>OuvrirProcédureStockée</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord la procédure stockée portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="12d00-117">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12d00-118"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="12d00-118"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="12d00-p104">Affichage dans lequel s’ouvre la procédure stockée. Cliquez sur <strong>Feuille de données</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Feuille de données</strong>.</span><span class="sxs-lookup"><span data-stu-id="12d00-p104">The view in which the stored procedure will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12d00-122"><strong>Mode Données</strong></span><span class="sxs-lookup"><span data-stu-id="12d00-122"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="12d00-p105">Mode de saisie de données de la procédure stockée. S’applique uniquement aux procédures stockées ouvertes en mode Feuille de données. Cliquez sur <strong>Ajouter</strong> (l’utilisateur ne peut ni afficher ni modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l’utilisateur peut afficher et modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> (l’utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>.</span><span class="sxs-lookup"><span data-stu-id="12d00-p105">The data entry mode for the stored procedure. This applies only to stored procedures opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="12d00-127">Notes</span><span class="sxs-lookup"><span data-stu-id="12d00-127">Remarks</span></span>

<span data-ttu-id="12d00-128">Cette action équivaut à double-cliquer sur la procédure stockée dans le volet de navigation ou à cliquer avec le bouton droit sur la procédure stockée dans le volet de navigation, puis à sélectionner la commande de votre choix.</span><span class="sxs-lookup"><span data-stu-id="12d00-128">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="12d00-p106">Basculer en mode Création lorsque la procédure stockée est ouverte supprime le paramètre de l’argument **Mode Données** de la procédure stockée. Ce paramètre n’est pas actif, même si l’utilisateur revient en mode Feuille de données.</span><span class="sxs-lookup"><span data-stu-id="12d00-p106">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure. This setting is not in effect, even if the user returns to Datasheet view.</span></span>


> [!TIP]
> <P></P>
> <UL>
> <LI>
> <P><span data-ttu-id="12d00-131">Vous pouvez faire glisser une procédure stockée à partir du volet de Navigation vers une ligne d’action de macro.</span><span class="sxs-lookup"><span data-stu-id="12d00-131">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="12d00-132">Cette opération crée automatiquement une action <STRONG>OuvrirProcédureStockée</STRONG> qui ouvre la procédure stockée en mode feuille de données.</span><span class="sxs-lookup"><span data-stu-id="12d00-132">This automatically creates an <STRONG>OpenStoredProcedure</STRONG> action that opens the stored procedure in Datasheet view.</span></span></P>
> <LI>
> <P><span data-ttu-id="12d00-133">
> 						Si vous ne voulez pas afficher les messages système qui s’affichent normalement lorsqu’une procédure stockée est exécutée (indiquant qu’il s’agit d’une procédure stockée et affichant le nombre d’enregistrements concernés), vous pouvez faire appel à l’action <STRONG>Avertissements</STRONG> pour supprimer l’affichage de ces messages.
</span><span class="sxs-lookup"><span data-stu-id="12d00-133">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the <STRONG>SetWarning</STRONG> action to suppress the display of these messages.</span></span></P></LI></UL>
<P></P>



<span data-ttu-id="12d00-134">Pour exécuter l’action **OuvrirProcédureStockée** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenStoredProcedure** de l’objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="12d00-134">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

