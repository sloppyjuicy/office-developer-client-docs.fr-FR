---
title: SélectionnerObjet, action de macro
TOCTitle: SelectObject Macro Action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 655b5c9273e84be3365116c2e7b93c657c0d732f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884057"
---
# <a name="selectobject-macro-action"></a><span data-ttu-id="e7016-102">SélectionnerObjet, action de macro</span><span class="sxs-lookup"><span data-stu-id="e7016-102">SelectObject Macro Action</span></span>


<span data-ttu-id="e7016-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7016-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7016-104">Vous pouvez utiliser l'action **SélectionnerObjet** pour sélectionner un objet de base de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="e7016-104">You can use the **SelectObject** action to select a specified database object.</span></span>

## <a name="setting"></a><span data-ttu-id="e7016-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7016-105">Setting</span></span>

<span data-ttu-id="e7016-106">L'action **SélectionnerObjet** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="e7016-106">The **SelectObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7016-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="e7016-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e7016-108">Description</span><span class="sxs-lookup"><span data-stu-id="e7016-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7016-109"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="e7016-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="e7016-p101">Type d’objet de base de données à sélectionner. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e7016-p101">The type of database object to select. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7016-113"><strong>Nom de l'objet</strong></span><span class="sxs-lookup"><span data-stu-id="e7016-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="e7016-p102">Nom de l’objet à sélectionner. La zone <strong>Nom de l’objet</strong> montre tous les objets de la base de données du type sélectionné par l’argument <strong>Type d’objet</strong>. Cet argument est obligatoire sauf si vous attribuez la valeur <strong>Oui</strong> à l’argument Dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="e7016-p102">The name of the object to select. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. This is a required argument, unless you set the In Navigation Pane argument to <strong>Yes</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="e7016-117">Les noms des objets <STRONG>Vue serveur</STRONG>, <STRONG>Schéma</STRONG> ou <STRONG>Procédure stockée</STRONG> ne sont pas affichés dans la zone <STRONG>Nom de l’objet</STRONG> d’un projet Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="e7016-117">The object names for <STRONG>Server View</STRONG>, <STRONG>Diagram</STRONG>, or <STRONG>Stored Procedure</STRONG> objects are not displayed in the <STRONG>Object Name</STRONG> box of an Access project (.adp).</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7016-118"><strong>Dans le volet de navigation</strong></span><span class="sxs-lookup"><span data-stu-id="e7016-118"><strong>In Navigation Pane</strong></span></span></p></td>
<td><p><span data-ttu-id="e7016-p103">Spécifie si Microsoft Office Access sélectionne l’objet dans le volet de navigation. Cliquez sur <strong>Oui</strong> (pour sélectionner l’objet dans le volet de navigation) ou sur <strong>Non</strong> (pour ne pas le sélectionner). <strong>Non</strong> est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7016-p103">Specifies whether Microsoft Access selects the object in the Navigation Pane. Click <strong>Yes</strong> (to select the object in the Navigation Pane) or <strong>No</strong> (not to select the object in the Navigation Pane). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e7016-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e7016-122">Remarks</span></span>

<span data-ttu-id="e7016-p104">L'action **SélectionnerObjet** fonctionne avec n'importe quel objet Access qui peut recevoir le focus. Cette action active (ou place le focus sur) l'objet spécifié et affiche l'objet s'il est masqué. Si l'objet est un formulaire, l'action **SélectionnerObjet** définit la propriété **Visible** du formulaire sur **Oui** et retourne le formulaire dans le mode défini par ses propriétés de formulaire (par exemple, sous la forme d'un formulaire modal ou d'un formulaire contextuel).</span><span class="sxs-lookup"><span data-stu-id="e7016-p104">The **SelectObject** action works with any Access object that can receive the focus. This action gives the specified object the focus and shows the object if it's hidden. If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).</span></span>

<span data-ttu-id="e7016-p105">Si l'objet n'est pas ouvert dans une des autres fenêtres Access, vous pouvez le sélectionner dans le volet de navigation en attribuant à l'argument **Dans le volet de navigation** la valeur **Oui**. Si l'argument **Dans le volet de navigation** a la valeur **Non**, un message d'erreur s'affiche lorsque vous essayez de sélectionner un objet qui n'est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="e7016-p105">If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**. If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.</span></span>

<span data-ttu-id="e7016-p106">Cette action est souvent utilisée pour sélectionner un objet sur lequel vous voulez effectuer des actions supplémentaires. Si Access est configuré pour utiliser des fenêtres superposées au lieu de documents à onglets, vous pouvez, par exemple, restaurer un objet qui a été réduit (avec l'action **RestaurerFenêtre** ) ou agrandir une fenêtre contenant un objet que vous voulez manipuler (avec l'action **AgrandirFenêtre** ).</span><span class="sxs-lookup"><span data-stu-id="e7016-p106">Often, you might use this action to select an object on which you want to perform additional actions. For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).</span></span>

<span data-ttu-id="e7016-p107">Si vous sélectionnez un formulaire, vous pouvez utiliser les actions **AtteindreContrôle**, **AtteindreEnregistrement** et **AtteindrePage** pour accéder à des zones spécifiques du formulaire. L'action **AtteindreEnregistrement** fonctionne également avec les feuilles de données.</span><span class="sxs-lookup"><span data-stu-id="e7016-p107">If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form. The **GoToRecord** action also works for datasheets.</span></span>

<span data-ttu-id="e7016-132">Pour exécuter l'action **SélectionnerObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SelectObject** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e7016-132">To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.</span></span>

