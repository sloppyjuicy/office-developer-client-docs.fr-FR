---
title: Parcourir, action de Macro
TOCTitle: BrowseTo Macro Action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 15009ca039d5df06bc732f4b58c066ad8f8d67c9
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603762"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="dac4f-102">Parcourir, action de Macro</span><span class="sxs-lookup"><span data-stu-id="dac4f-102">BrowseTo Macro Action</span></span>

<span data-ttu-id="dac4f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dac4f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dac4f-p101">Vous pouvez utiliser l'action **Parcourir** pour naviguer parmi des objets en place. Vous pouvez également modifier l'objet source d'un contrôle de sous-formulaire en spécifiant l'argument Chemin d'accès au contrôle de sous-formulaire. Utilisez **Parcourir** pour naviguer de formulaire1 à formulaire2 sans ouvrir de nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dac4f-p101">You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="dac4f-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dac4f-107">Setting</span></span>

<span data-ttu-id="dac4f-108">L'action **Parcourir** utilise l'argument suivant :</span><span class="sxs-lookup"><span data-stu-id="dac4f-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dac4f-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="dac4f-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dac4f-110">Description</span><span class="sxs-lookup"><span data-stu-id="dac4f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dac4f-111">Type d'objet</span><span class="sxs-lookup"><span data-stu-id="dac4f-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="dac4f-112">Type d'objet vers lequel naviguer.</span><span class="sxs-lookup"><span data-stu-id="dac4f-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dac4f-113">Nom d’objet</span><span class="sxs-lookup"><span data-stu-id="dac4f-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="dac4f-114">Objet qui se charge à l’intérieur du contrôle de sous-formulaire référencé par l’argument Chemin d’accès au contrôle de sous-formulaire.</span><span class="sxs-lookup"><span data-stu-id="dac4f-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dac4f-115">Chemin d’accès au contrôle de sous-formulaire</span><span class="sxs-lookup"><span data-stu-id="dac4f-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="dac4f-116">Si spécifié, le chemin d’accès à partir du formulaire principal de l’application du sous-formulaire cible contrôle qui charge l’objet spécifié par l’argument nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dac4f-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dac4f-117">Condition Where</span><span class="sxs-lookup"><span data-stu-id="dac4f-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="dac4f-118">Spécifié, remplace la condition Where de la source de l'enregistrement de l'objet.</span><span class="sxs-lookup"><span data-stu-id="dac4f-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dac4f-119">Page</span><span class="sxs-lookup"><span data-stu-id="dac4f-119">Page</span></span></p></td>
<span data-ttu-id="dac4f-120"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="dac4f-120"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="dac4f-p102">Spécifié, définit la page du formulaire continu qui deviendra la page active. Cet argument est réservé au Web.</span><span class="sxs-lookup"><span data-stu-id="dac4f-p102">If specified, sets the page of the continuous form that will be made the current page. This argument is Web only.</span></span></p></td>
=======
<td><p><span data-ttu-id="dac4f-123">Spécifié, définit la page du formulaire continu qui deviendra la page active.</span><span class="sxs-lookup"><span data-stu-id="dac4f-123">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="dac4f-124">Cet argument est web uniquement.</span><span class="sxs-lookup"><span data-stu-id="dac4f-124">This argument is web only.</span></span></p></td><span data-ttu-id="dac4f-125">
>>>>>>>forme de base</span><span class="sxs-lookup"><span data-stu-id="dac4f-125">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dac4f-126">Mode Données</span><span class="sxs-lookup"><span data-stu-id="dac4f-126">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="dac4f-127">Spécifié, le mode d'entrée des données du formulaire.</span><span class="sxs-lookup"><span data-stu-id="dac4f-127">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dac4f-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="dac4f-128">Remarks</span></span>

<span data-ttu-id="dac4f-129">L'argument Chemin d'accès au contrôle de sous-formulaire doit être spécifié à l'aide de la syntaxe de l'exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="dac4f-129">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="dac4f-p104">Dans cet exemple, le Formulaire principal est le formulaire de niveau supérieur dans l'application cliente Access. L'argument Chemin d'accès au contrôle de sous-formulaire doit spécifier en alternance les noms des contrôles de sous-formulaire et formulaire menant du formulaire principal au contrôle de sous-formulaire qui est le conteneur de l'objet spécifié par l'argument Nom d'objet. Chaque contrôle de sous-formulaire spécifié doit être un contrôle sur le formulaire qui le précède. Le chemin d'accès doit se terminer par un contrôle de sous-formulaire.</span><span class="sxs-lookup"><span data-stu-id="dac4f-p104">In this example, the Main Form is the top level form in the Access client application. The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument. Each subform control specified must be a control on the form that precedes it. The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="dac4f-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="dac4f-134">Example</span></span>

<span data-ttu-id="dac4f-135">L’exemple suivant montre comment utiliser l’action Parcourir pour ouvrir un état dans un contrôle de sous-formulaire ou dans un contrôle de navigation.</span><span class="sxs-lookup"><span data-stu-id="dac4f-135">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="dac4f-136">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="dac4f-136">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```



