---
title: RedessinerObjet, action de macro
TOCTitle: RepaintObject Macro Action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 431baa0e98d0ae3a636cb93fd799c3bdf4450816
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882608"
---
# <a name="repaintobject-macro-action"></a><span data-ttu-id="9b067-102">RedessinerObjet, action de macro</span><span class="sxs-lookup"><span data-stu-id="9b067-102">RepaintObject Macro Action</span></span>


<span data-ttu-id="9b067-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b067-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b067-p101">Vous pouvez utiliser l'action **RedessinerObjet** pour effectuer les mises à jour d'écran en attente pour l'objet de base de données spécifié ou pour celui actif si aucun objet n'est spécifié. Ces mises à jour englobent les nouveaux calculs en attente des contrôles de l'objet.</span><span class="sxs-lookup"><span data-stu-id="9b067-p101">You can use the **RepaintObject** action to complete any pending screen updates for a specified database object or for the active database object, if none is specified. Such updates include any pending recalculations for the object's controls.</span></span>

## <a name="setting"></a><span data-ttu-id="9b067-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b067-106">Setting</span></span>

<span data-ttu-id="9b067-107">L'action **RedessinerObjet** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="9b067-107">The **RepaintObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b067-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="9b067-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9b067-109">Description</span><span class="sxs-lookup"><span data-stu-id="9b067-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b067-110"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="9b067-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="9b067-p102">Type d’objet à redessiner. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Laissez cet argument vide pour sélectionner l’objet actif.</span><span class="sxs-lookup"><span data-stu-id="9b067-p102">The type of object to repaint. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b067-114"><strong>Nom de l'objet</strong></span><span class="sxs-lookup"><span data-stu-id="9b067-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9b067-p103">Nom de l’objet à redessiner. La zone <strong>Nom de l’objet</strong> affiche tous les objets dans la base de données dont le type correspond à celui sélectionné par l’argument <strong>Type d’objet</strong>. Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez cet argument également vide.</span><span class="sxs-lookup"><span data-stu-id="9b067-p103">The name of the object to repaint. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9b067-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9b067-118">Remarks</span></span>

<span data-ttu-id="9b067-p104">Pour achever des mises à jour d'écran en attente, Microsoft Office Access attend d'avoir terminé d'autres tâches en attente. Avec cette action, vous pouvez faire en sorte que tous les contrôles de l'objet spécifié soient immédiatement redessinés. Vous pouvez utiliser cette action dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="9b067-p104">Microsoft Access waits to complete pending screen updates until it finishes other pending tasks. With this action, you can force immediate repainting of the controls in the specified object. You can use this action:</span></span>

  - <span data-ttu-id="9b067-p105">Lorsque vous utilisez l'action **DéfinirValeur** pour modifier des valeurs dans une série de contrôles. Access n'affiche pas toujours immédiatement les modifications, surtout si d'autres contrôles (tels que des contrôles calculés) dépendent des valeurs des contrôles modifiés.</span><span class="sxs-lookup"><span data-stu-id="9b067-p105">When you use the **SetValue** action to change values in a number of controls. Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span></span>

  - <span data-ttu-id="9b067-p106">Lorsque vous voulez être certain que le formulaire affiché montre les données de tous ses contrôles. Par exemple, des contrôles contenant des objets OLE n'affichent pas immédiatement leurs données après que vous avez ouvert un formulaire.</span><span class="sxs-lookup"><span data-stu-id="9b067-p106">When you want to make sure that the form you are viewing displays data in all of its controls. For example, controls containing OLE objects don't display their data immediately after you open a form.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="9b067-p107">Dans la mesure où cette action n'entraîne pas de réactualisation de la base de données, elle n'affiche pas les enregistrements nouveaux et modifiés pas plus qu'elle ne supprime les enregistrements supprimés de la table ou requête sous-jacente de l'objet. Utilisez l'action <STRONG>Actualiser</STRONG> pour actualiser la source de l'objet ou l'un de ses contrôles. Utilisez l'action <STRONG>AfficherTousEnreg</STRONG> pour afficher les enregistrements les plus récents et supprimer tous les filtres.</span><span class="sxs-lookup"><span data-stu-id="9b067-p107">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query. Use the <STRONG>Requery</STRONG> action to requery the source of the object or one of its controls. Use the <STRONG>ShowAllRecords</STRONG> action to display the most recent records and remove any applied filters.</span></span></P>
> <LI>
> <P><span data-ttu-id="9b067-129">L'action <STRONG>RedessinerObjet</STRONG> n'a pas le même effet que l'option <STRONG>Actualiser</STRONG> dans le groupe <STRONG>Enregistrements</STRONG> de l'onglet <STRONG>Accueil</STRONG>, laquelle affiche toutes les modifications que vous ou d'autres utilisateurs avez apportées aux enregistrements actuellement affichés dans des formulaires et des feuilles de données.</span><span class="sxs-lookup"><span data-stu-id="9b067-129">The <STRONG>RepaintObject</STRONG> action doesn't have the same effect as clicking <STRONG>Refresh</STRONG> in the <STRONG>Records</STRONG> group on the <STRONG>Home</STRONG> tab, which shows any changes you or other users have made to the currently displayed records in forms and datasheets.</span></span></P></LI></UL>



<span data-ttu-id="9b067-130">Pour exécuter l'action **RedessinerObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **RepaintObject** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="9b067-130">To run the **RepaintObject** action in a Visual Basic for Applications (VBA) module, use the **RepaintObject** method of the **DoCmd** object.</span></span>

