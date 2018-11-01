---
title: FermerFenêtre, action de macro
TOCTitle: CloseWindow Macro Action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ab6b3a265b6e63680add41ec051ba61a262819bd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876840"
---
# <a name="closewindow-macro-action"></a><span data-ttu-id="4eb2e-102">FermerFenêtre, action de macro</span><span class="sxs-lookup"><span data-stu-id="4eb2e-102">CloseWindow Macro Action</span></span>


<span data-ttu-id="4eb2e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4eb2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4eb2e-104">Vous pouvez utiliser l’action **Fermerfenêtre** pour fermer un onglet de document d’accès spécifié ou de l’onglet de document actif si aucun n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="4eb2e-104">You can use the **CloseWindow** action to close either a specified Access document tab or the active document tab if none is specified.</span></span>

## <a name="setting"></a><span data-ttu-id="4eb2e-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="4eb2e-105">Setting</span></span>

<span data-ttu-id="4eb2e-106">L'action **FermerFenêtre** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4eb2e-106">The **CloseWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4eb2e-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="4eb2e-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4eb2e-108">Description</span><span class="sxs-lookup"><span data-stu-id="4eb2e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4eb2e-109"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="4eb2e-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="4eb2e-p101">Type d’objet dont vous voulez fermer l’onglet de document. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Pour sélectionner l’onglet de document actif, laissez cet argument vide. 

</span><span class="sxs-lookup"><span data-stu-id="4eb2e-p101">The type of object whose document tab you want to close. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active document tab, leave this argument blank.</span></span></p>

> [!NOTE]
> <span data-ttu-id="4eb2e-113">Si vous fermez un module dans Visual Basic Editor, vous devez utiliser **Module** dans l’argument **Type d’objet**.</span><span class="sxs-lookup"><span data-stu-id="4eb2e-113">If you are closing a module in the Visual Basic Editor, you must use **Module** in the **Object Type** argument.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4eb2e-114"><strong>Nom de l'objet</strong></span><span class="sxs-lookup"><span data-stu-id="4eb2e-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4eb2e-p102">Nom de l’objet à fermer. La zone <strong>Nom de l’objet</strong> affiche tous les objets de la base de données correspondant au type sélectionné par l’argument <strong>Type d’objet</strong>. Cliquez sur l’objet pour le fermer. Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez également celui-ci vide.</span><span class="sxs-lookup"><span data-stu-id="4eb2e-p102">The name of the object to be closed. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. Click the object to close. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4eb2e-119"><strong>Save</strong></span><span class="sxs-lookup"><span data-stu-id="4eb2e-119"><strong>Save</strong></span></span></p></td>
<td><p><span data-ttu-id="4eb2e-p103">Indique si les modifications apportées à l’objet doivent être enregistrées à la fermeture. Cliquez sur <strong>Oui</strong> (enregistrer l’objet), sur <strong>Non</strong> (fermer l’objet sans enregistrer) ou sur <strong>Avec confirmation</strong> (demander à l’utilisateur d’enregistrer ou non l’objet). La valeur par défaut est <strong>Avec confirmation</strong>.</span><span class="sxs-lookup"><span data-stu-id="4eb2e-p103">Whether to save changes to the object when it is closed. Click <strong>Yes</strong> (save the object), <strong>No</strong> (close the object without saving it), or <strong>Prompt</strong> (prompt the user whether or not to save the object). The default is <strong>Prompt</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4eb2e-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="4eb2e-123">Remarks</span></span>

<span data-ttu-id="4eb2e-p104">L'action **FermerFenêtre** fonctionne sur tous les objets de base de données que l'utilisateur peut ouvrir ou fermer explicitement. Cette action équivaut à sélectionner un objet, puis à le fermer en cliquant avec le bouton droit sur l'onglet de document de l'objet, puis en cliquant sur le bouton **Fermer** dans le menu contextuel ou en cliquant sur le bouton **Fermer** de l'objet.</span><span class="sxs-lookup"><span data-stu-id="4eb2e-p104">The **CloseWindow** action works on all database objects that the user can explicitly open or close. This action has the same effect as selecting an object and then closing it by right-clicking the object's document tab and then clicking **Close** on the shortcut menu, or clicking the **Close** button for the object.</span></span>

<span data-ttu-id="4eb2e-p105">Si l'argument **Enregistrer** est défini sur **Avec confirmation** et que l'objet n'a pas encore été enregistré au moment de l'exécution de l'action **FermerFenêtre**, une boîte de dialogue demande à l'utilisateur d'enregistrer l'objet avant que la macro ne le ferme. Si vous avez défini l'argument **Avertissements actifs** de l'action **Avertissements** sur **Non**, la boîte de dialogue n'est pas affichée et l'objet est automatiquement enregistré.</span><span class="sxs-lookup"><span data-stu-id="4eb2e-p105">If the **Save** argument is set to **Prompt** and the object hasn't already been saved before the **CloseWindow** action is carried out, a dialog box prompts the user to save the object before the macro closes it. If you have set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box is not displayed and the object is automatically saved.</span></span>

<span data-ttu-id="4eb2e-128">Pour exécuter l'action **FermerFenêtre** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Close** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="4eb2e-128">To run the **CloseWindow** action in a Visual Basic for Applications (VBA) module, use the **CloseWindow** method of the **DoCmd** object.</span></span>

