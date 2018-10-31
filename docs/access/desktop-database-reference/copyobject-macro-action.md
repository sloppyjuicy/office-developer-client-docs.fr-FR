---
title: CopierObjet, action de macro
TOCTitle: CopyObject Macro Action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 60c0204bd374feaa950d3158873f68127debaf0f
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862547"
---
# <a name="copyobject-macro-action"></a><span data-ttu-id="9877e-102">CopierObjet, action de macro</span><span class="sxs-lookup"><span data-stu-id="9877e-102">CopyObject Macro Action</span></span>


<span data-ttu-id="9877e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9877e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9877e-p101">Utilisez l'action **CopierObjet** pour copier l'objet de base de données spécifié dans une autre base de données Access ou dans la même base ou projet Access mais sous un nouveau nom. Par exemple, vous pouvez copier ou enregistrer un objet existant dans une autre base de données ou créer rapidement un objet similaire en n'apportant que quelques modifications.</span><span class="sxs-lookup"><span data-stu-id="9877e-p101">You can use the **CopyObject** action to copy the specified database object to a different Access database or to the same database or Access project under a new name. For example, you can copy or back up an existing object in another database or quickly create a similar object with a few changes.</span></span>


> [!NOTE]
> <span data-ttu-id="9877e-p102">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="9877e-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



## <a name="setting"></a><span data-ttu-id="9877e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="9877e-108">Setting</span></span>

<span data-ttu-id="9877e-109">L'action **CopierObjet** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="9877e-109">The **CopyObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9877e-110">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="9877e-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9877e-111">Description</span><span class="sxs-lookup"><span data-stu-id="9877e-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9877e-112"><strong>Base de données de destination</strong></span><span class="sxs-lookup"><span data-stu-id="9877e-112"><strong>Destination Database</strong></span></span></p></td>
<td><p><span data-ttu-id="9877e-p103">Chemin d’accès valide et nom de fichier de la base de données de destination. Entrez le chemin d’accès et le nom de fichier dans la zone <strong>Base de données de destination</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Laissez cet argument vide si vous souhaitez sélectionner la base de données active. 

</span><span class="sxs-lookup"><span data-stu-id="9877e-p103">A valid path and file name for the destination database. Enter the path and file name in the <strong>Destination Database</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank if you want to select the current database.</span></span></p>

> [!NOTE]
> <span data-ttu-id="9877e-p104">Cet argument n’est disponible que dans l’environnement de base de données Access. Si cette action est utilisée dans un environnement de projet Access (.adp), l’argument Base de données de destination doit être vide.</span><span class="sxs-lookup"><span data-stu-id="9877e-p104">This argument is only available in the Access database environment. When using this action in an Access project environment (.adp), the Destination Database argument must be blank.</span></span>


<p><span data-ttu-id="9877e-118">Si vous exécutez une macro contenant l’action <strong>CopierObjet</strong> dans une base de données bibliothèque et que vous laissez cet argument vide, Microsoft Office Access 2007 copie l’objet dans la base de données bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="9877e-118">If you run a macro containing the <strong>CopyObject</strong> action in a library database and leave this argument blank, Microsoft Office Access 2007 will copy the object into the library database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9877e-119"><strong>Nouveau nom</strong></span><span class="sxs-lookup"><span data-stu-id="9877e-119"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9877e-p105">Nouveau nom de l’objet. En cas de copie dans une base de données différente, laissez cet argument vide pour conserver le même nom.</span><span class="sxs-lookup"><span data-stu-id="9877e-p105">A new name for the object. When copying to a different database, leave this argument blank to keep the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9877e-122"><strong>Type d’objet source</strong></span><span class="sxs-lookup"><span data-stu-id="9877e-122"><strong>Source Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="9877e-p106">Type d’objet à copier. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong>. Pour copier l’objet sélectionné dans le volet de navigation, laissez cet argument vide.</span><span class="sxs-lookup"><span data-stu-id="9877e-p106">The object type you want to copy. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To copy the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9877e-126"><strong>Nom de l’objet source</strong></span><span class="sxs-lookup"><span data-stu-id="9877e-126"><strong>Source Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9877e-127">Le nom de l’objet à copier.</span><span class="sxs-lookup"><span data-stu-id="9877e-127">The name of the object to be copied.</span></span> <span data-ttu-id="9877e-128">La zone <strong>Nom de l’objet Source</strong> affiche tous les objets dans la base de données du type sélectionné par l’argument <strong>Type d’objet Source</strong> .</span><span class="sxs-lookup"><span data-stu-id="9877e-128">The <strong>Source Object Name</strong> box shows all objects in the database of the type selected by the <strong>Source Object Type</strong> argument.</span></span> <span data-ttu-id="9877e-129">Dans la zone <strong>Nom de l’objet Source</strong> , cliquez sur l’objet à copier.</span><span class="sxs-lookup"><span data-stu-id="9877e-129">In the <strong>Source Object Name</strong> box, click the object to copy.</span></span> <span data-ttu-id="9877e-130">Si vous laissez l’argument <strong>Type d’objet Source</strong> vide, laissez également cet argument vide.</span><span class="sxs-lookup"><span data-stu-id="9877e-130">If you leave the <strong>Source Object Type</strong> argument blank, leave this argument blank also.</span></span> <span data-ttu-id="9877e-131">Si vous exécutez une macro contenant l’action <strong>CopierObjet</strong> dans une base de données bibliothèque, Access commence par rechercher un objet portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="9877e-131">If you run a macro containing the <strong>CopyObject</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9877e-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="9877e-132">Remarks</span></span>

<span data-ttu-id="9877e-133">Vous devez entrer une valeur pour l'argument **Base de données de destination** et/ou **Nouveau nom** pour cette action.</span><span class="sxs-lookup"><span data-stu-id="9877e-133">You must enter a value for either one or both of the **Destination Database** and **New Name** arguments for this action.</span></span>

<span data-ttu-id="9877e-p108">Si vous laissez les arguments **Type d'objet source** et **Nom de l'objet source** vides, Access copie l'objet sélectionné dans le volet de navigation. Pour sélectionner un objet dans le volet de navigation, vous pouvez utiliser l'action **SélectionnerObjet** avec l'argument DansVoletDeNavigation défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="9877e-p108">If you leave the **Source Object Type** and **Source Object Name** arguments blank, Access copies the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the In Navigation Pane argument set to **Yes**.</span></span>

<span data-ttu-id="9877e-136">L'action **CopierObjet** équivaut à réaliser les étapes suivantes manuellement :</span><span class="sxs-lookup"><span data-stu-id="9877e-136">The **CopyObject** action is similar to performing the following steps manually:</span></span>

1.  <span data-ttu-id="9877e-137">Sélectionnez un objet dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="9877e-137">Select an object in the Navigation Pane.</span></span>

2.  <span data-ttu-id="9877e-138">Sous l'onglet Home, dans le groupe Clipboard, cliquez sur Copy.</span><span class="sxs-lookup"><span data-stu-id="9877e-138">On the Home tab, in the Clipboard group, click Copy.</span></span>

3.  <span data-ttu-id="9877e-p109">Sous le même onglet, cliquez sur **Coller**.La boîte de dialogue **Coller sous** s'affiche afin que vous puissiez donner un nouveau nom à l'objet. L'action **CopierObjet** effectue toutes ces étapes automatiquement.</span><span class="sxs-lookup"><span data-stu-id="9877e-p109">On the same tab, click **Paste**.The **Paste As** dialog box appears so that you can give the object a new name. The **CopyObject** action performs all of these steps automatically.</span></span>


> [!NOTE]
> <span data-ttu-id="9877e-141">[!REMARQUE] Lors de la copie des pages d'accès aux données, l'action **CopierObjet** copie uniquement le lien vers le fichier .htm associé, pas le fichier lui-même.</span><span class="sxs-lookup"><span data-stu-id="9877e-141">When copying data access pages, the **CopyObject** action copies only the link to the associated .htm file, not the file itself.</span></span>



<span data-ttu-id="9877e-p110">Le chemin d'accès et le nom de fichier de la base de données de destination doivent exister préalablement à l'exécution de l'action **CopierObjet** par la macro. S'ils n'existent pas, Access affiche un message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="9877e-p110">The path and file name of the destination database must exist before the macro runs the **CopyObject** action. If they don't exist, Access displays an error message.</span></span>

<span data-ttu-id="9877e-144">Pour exécuter l'action **CopierObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **CopyObject** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="9877e-144">To run the **CopyObject** action in a Visual Basic for Applications (VBA) module, use the **CopyObject** method of the **DoCmd** object.</span></span>

<span data-ttu-id="9877e-p111">Vous pouvez également copier manuellement un objet sélectionné dans le volet de navigation ou un objet qui est actuellement ouvert en cliquant sur l'onglet **Fichier**, puis sur **Enregistrer sous**. Cette commande fait une copie de l'objet dans la base de données active uniquement. Dans la boîte de dialogue **Enregistrer sous**, entrez le nom de la copie et choisissez le type d'objet sous lequel vous voulez l'enregistrer. Si l'objet d'origine a déjà été enregistré et que vous l'enregistrez dans la base de données active sous un nouveau nom, la version d'origine est conservée sous son ancien nom.</span><span class="sxs-lookup"><span data-stu-id="9877e-p111">You can also manually copy an object selected in the Navigation Pane, or an object that is currently open, by clicking the **File** tab and then clicking **Save As**. This command will make a copy of the object in the current database only. In the **Save As** dialog box, enter the name for the copy, and choose what type of object you want to save it as. If the original object has already been saved and you save it in the current database with a new name, the original version still exists with its old name.</span></span>

<span data-ttu-id="9877e-149">Pour copier manuellement un objet dans une base de données Access différente :</span><span class="sxs-lookup"><span data-stu-id="9877e-149">To manually copy an object to a different Access database:</span></span>

1.  <span data-ttu-id="9877e-150">Sous l'onglet **Données externes**, dans le groupe **Exporter**, cliquez sur **Autres**, puis cliquez sur **Base de données Access**.</span><span class="sxs-lookup"><span data-stu-id="9877e-150">On the **External Data** tab, in the **Export** group, click **More** and then click **Access Database**.</span></span>

2.  <span data-ttu-id="9877e-151">Dans la boîte de dialogue **Exportation - Base de données Access**, entrez le nom de fichier de la base de données de destination.- ou -Cliquez sur **Parcourir** pour afficher la boîte de dialogue **Enregistrer**, recherchez la base de données de destination, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9877e-151">In the **Export - Access Database** dialog box, enter the file name of the destination database.-or-Click **Browse** to display the **File Save** dialog box, locate the destination database, and then click **Save**.</span></span>

3.  <span data-ttu-id="9877e-p112">Dans la boîte de dialogue **Exportation - Base de données Access**, cliquez sur **OK**. La boîte de dialogue **Exporter** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="9877e-p112">In the **Export - Access Database** dialog box, click **OK**. The **Export** dialog box appears.</span></span>

4.  <span data-ttu-id="9877e-p113">Dans la boîte de dialogue **Exporter**, entrez le nom de l'objet dans la base de données de destination. Choisissez les options appropriées, comme **Définition et données** ou **Définition uniquement** pour les tables. Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="9877e-p113">In the **Export** dialog box, enter a name for the object in the destination database. Choose any applicable options, such as **Export Definition and Data** or **Definition Only** for tables. When you are finished, click **OK**.</span></span>

