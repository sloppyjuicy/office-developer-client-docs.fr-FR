---
title: SaveObject, action de macro
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf6fe02616134f864a0e07092951ab9cf49aadbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308931"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="86ed2-102">SaveObject, action de macro</span><span class="sxs-lookup"><span data-stu-id="86ed2-102">SaveObject macro action</span></span>

<span data-ttu-id="86ed2-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86ed2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86ed2-p101">Vous pouvez utiliser l'action **EnregistrerObjet** pour enregistrer un objet Access spécifié ou l'objet actif si aucun n'est spécifié. Vous pouvez également enregistrer l'objet actif sous un nouveau nom dans certains cas (cela équivaut à utiliser la commande **Enregistrer sous** dans la **barre d'outils Accès rapide**).</span><span class="sxs-lookup"><span data-stu-id="86ed2-p101">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified. You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>

> [!NOTE]
> <span data-ttu-id="86ed2-106">Cette action ne sera pas autorisée si la base de données n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="86ed2-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="86ed2-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="86ed2-107">Setting</span></span>

<span data-ttu-id="86ed2-108">L’action **EnregistrerObjet** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="86ed2-108">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86ed2-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="86ed2-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="86ed2-110">Description</span><span class="sxs-lookup"><span data-stu-id="86ed2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86ed2-111"><strong>Type d’objet</strong></span><span class="sxs-lookup"><span data-stu-id="86ed2-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="86ed2-p102">Type d’objet à enregistrer. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> dans le volet Générateur de macro. Pour sélectionner l’objet actif, laissez cet argument vide. Si vous sélectionnez un type d’objet, vous devez sélectionner un nom d’objet existant dans l’argument <strong>Nom de l’objet</strong>.</span><span class="sxs-lookup"><span data-stu-id="86ed2-p102">The type of object you want to save. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active object, leave this argument blank. If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86ed2-116"><strong>Nom objet</strong></span><span class="sxs-lookup"><span data-stu-id="86ed2-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="86ed2-117">Nom de l’objet à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="86ed2-117">The name of the object to be saved.</span></span> <span data-ttu-id="86ed2-118">La zone <strong>Nom de l’objet</strong> montre tous les objets de la base de données du type sélectionné par l’argument <strong>Type d’objet</strong>.</span><span class="sxs-lookup"><span data-stu-id="86ed2-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="86ed2-119">Si vous ne spécifiez rien dans l’argument <strong>Type d’objet</strong>, vous pouvez laisser cet argument vide pour enregistrer l’objet actif ou, dans certains cas, entrer un nouveau nom dans cet argument pour enregistrer l’objet actif sous ce nom.</span><span class="sxs-lookup"><span data-stu-id="86ed2-119">If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name.</span></span> <span data-ttu-id="86ed2-120">Si vous entrez un nouveau nom, ce dernier doit respecter les conventions d’appellation des objets Microsoft Office Access.</span><span class="sxs-lookup"><span data-stu-id="86ed2-120">If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="86ed2-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="86ed2-121">Remarks</span></span>

<span data-ttu-id="86ed2-122">L'action **EnregistrerObjet** s'applique à tous les objets de base de données que l'utilisateur peut explicitement ouvrir et enregistrer.</span><span class="sxs-lookup"><span data-stu-id="86ed2-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="86ed2-123">L'objet spécifié doit être ouvert pour que l'action **EnregistrerObjet** puisse être appliquée à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="86ed2-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="86ed2-124">Cette action équivaut à sélectionner un objet puis à l'enregistrer en cliquant sur **Enregistrer** dans la **barre d'outils Accès rapide**.</span><span class="sxs-lookup"><span data-stu-id="86ed2-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> 

<span data-ttu-id="86ed2-125">En laissant l'argument **Type d'objet** vide et en spécifiant un nouveau nom dans l'argument **Nom de l'objet**, vous obtenez le même résultat qu'en cliquant sur **Enregistrer sous** dans la **barre d'outils Accès rapide** et en indiquant un nouveau nom pour l'objet actif.</span><span class="sxs-lookup"><span data-stu-id="86ed2-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="86ed2-126">L'utilisation de l'action **EnregistrerObjet** vous permet de spécifier un objet à enregistrer et d'exécuter une commande **Enregistrer sous** à partir d'une macro.</span><span class="sxs-lookup"><span data-stu-id="86ed2-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>

> [!NOTE]
> <span data-ttu-id="86ed2-127">[!REMARQUE] Vous ne pouvez pas utiliser l'action **EnregistrerObjet** pour enregistrer un des éléments suivants sous un nouveau nom :</span><span class="sxs-lookup"><span data-stu-id="86ed2-127">You can't use the **SaveObject** action to save any of the following with a new name:</span></span>
> - <span data-ttu-id="86ed2-128">Un formulaire en mode formulaire ou en mode feuille de forme</span><span class="sxs-lookup"><span data-stu-id="86ed2-128">A form in Form view or Datasheet view</span></span>
> - <span data-ttu-id="86ed2-129">Un État en mode aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="86ed2-129">A report in Print Preview</span></span>
> - <span data-ttu-id="86ed2-130">Un module</span><span class="sxs-lookup"><span data-stu-id="86ed2-130">A module</span></span>
> - <span data-ttu-id="86ed2-131">Une vue serveur en mode feuille de en mode feuille de feuille ou aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="86ed2-131">A server view in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="86ed2-132">Page d'accès aux données en mode page</span><span class="sxs-lookup"><span data-stu-id="86ed2-132">A data access page in Page view</span></span>
> - <span data-ttu-id="86ed2-133">Une table en mode feuille de table ou aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="86ed2-133">A table in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="86ed2-134">Une requête en mode feuille de demande ou aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="86ed2-134">A query in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="86ed2-135">Une procédure stockée en mode feuille de feuille ou aperçu avant impression</span><span class="sxs-lookup"><span data-stu-id="86ed2-135">A stored procedure in Datasheet view or Print Preview</span></span>

<span data-ttu-id="86ed2-136">L'action **EnregistrerObjet** enregistre toujours l'objet spécifié ou l'objet actif dans la base de données qui a servi à créer l'objet, que cette action soit effectuée dans une macro exécutée dans la base de données active ou une base de données bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="86ed2-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="86ed2-p106">Si vous enregistrez l'objet actif sous un nouveau nom mais si ce nom est identique à celui d'un objet existant du même type, une boîte de dialogue vous demande si vous souhaitez remplacer l'objet existant. Si vous avez sélectionné la valeur **Non** pour l'argument **Avertissements actifs** de l'action **Avertissements**, la boîte de dialogue n'est pas affichée et l'ancien objet est automatiquement remplacé.</span><span class="sxs-lookup"><span data-stu-id="86ed2-p106">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object. If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="86ed2-139">Pour exécuter l'action **EnregistrerObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Save** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="86ed2-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

