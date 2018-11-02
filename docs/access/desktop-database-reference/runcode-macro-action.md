---
title: RunCode, action de macro
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
ms.openlocfilehash: acf8ed2bd10efd55436b8933a862833b8e49c5f0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926688"
---
# <a name="runcode-macro-action"></a><span data-ttu-id="5068d-102">RunCode, action de macro</span><span class="sxs-lookup"><span data-stu-id="5068d-102">RunCode macro action</span></span>


<span data-ttu-id="5068d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5068d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5068d-104">Vous pouvez utiliser l'action **ExécuterCode** pour appeler une procédure Function Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="5068d-104">You can use the **RunCode** action to call a Visual Basic for Applications (VBA) Function procedure.</span></span>

## <a name="setting"></a><span data-ttu-id="5068d-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="5068d-105">Setting</span></span>

<span data-ttu-id="5068d-106">L'action **ExécuterCode** accepte l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="5068d-106">The **RunCode** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5068d-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="5068d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5068d-108">Description</span><span class="sxs-lookup"><span data-stu-id="5068d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5068d-109"><strong>Nom de la fonction</strong></span><span class="sxs-lookup"><span data-stu-id="5068d-109"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5068d-p101">Nom de la procédure Function VBA à appeler. Placez tous les arguments de la fonction entre parenthèses. Entrez le nom de la fonction dans la zone <strong>Nom fonction</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5068d-p101">The name of the VBA Function procedure to call. Enclose any function arguments in parentheses. Enter the function name in the <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="5068d-p102">Dans une base de données Access (.mdb ou .accdb), cliquez sur le bouton <STRONG>Générateur</STRONG> pour sélectionner une fonction pour cet argument à l’aide du Générateur d’expressions. Cliquez sur la fonction de votre choix dans la liste proposée par le Générateur d’expression.</span><span class="sxs-lookup"><span data-stu-id="5068d-p102">In an Access database (.mdb or .accdb), click the <STRONG>Build</STRONG> button to use the Expression Builder to select a function for this argument. Click the desired function in the list in the Expression Builder.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5068d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5068d-116">Remarks</span></span>

<span data-ttu-id="5068d-117">Les procédures Function définies par l'utilisateur sont stockées dans des modules Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5068d-117">The user-defined Function procedures are stored in Microsoft Access modules.</span></span>

<span data-ttu-id="5068d-118">Vous devez inclure des parenthèses, même si la procédure Function ne prend aucun argument, comme dans l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="5068d-118">You must include parentheses, even if the Function procedure doesn't have any arguments, as in the following example:</span></span>

`TestFunction()`

<span data-ttu-id="5068d-119">Contrairement aux noms de fonction définie par l’utilisateur utilisés pour les paramètres de propriété d’événement, le nom de la fonction dans l’argument **Nom fonction** ne commence pas par un signe égal (**=**).</span><span class="sxs-lookup"><span data-stu-id="5068d-119">Unlike user-defined function names used for event property settings, the function name in the **Function Name** argument doesn't begin with an equal sign (**=**).</span></span>

<span data-ttu-id="5068d-120">Access ignore la valeur renvoyée par la fonction.</span><span class="sxs-lookup"><span data-stu-id="5068d-120">Access ignores the return value of the function.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5068d-121">[!REMARQUE] Vous ne pouvez pas appeler une procédure Function à partir d'une macro si le nom de la fonction est identique à celui du module.</span><span class="sxs-lookup"><span data-stu-id="5068d-121">You can't call a Function procedure from a macro if the function name is the same as the module name.</span></span></P>




> [!TIP]
> <P><span data-ttu-id="5068d-p103">[!CONSEIL] Pour exécuter une procédure Sub ou une procédure événementielle rédigée en Visual Basic, créez une procédure Function qui appelle la procédure Sub ou la procédure événementielle. Ensuite, utilisez l'action <STRONG>ExécuterCode</STRONG> pour exécuter la procédure Function.</span><span class="sxs-lookup"><span data-stu-id="5068d-p103">To run a Sub procedure or event procedure written in Visual Basic, create a Function procedure that calls the Sub procedure or event procedure. Then use the <STRONG>RunCode</STRONG> action to run the Function procedure.</span></span></P>



<span data-ttu-id="5068d-p104">Si vous utilisez l'action **ExécuterCode** pour appeler une fonction, Access recherche la fonction correspondant au nom spécifié par l'argument **Nom fonction** dans les modules standard de la base de données. Toutefois, lorsque cette action est exécutée en réponse à un clic d'une commande de menu dans un formulaire ou un état ou en réponse à un événement d'un formulaire ou d'un état, Access recherche d'abord la fonction dans le module de classe du formulaire ou de l'état, puis dans les modules standard. Access n'effectue pas de recherche dans les modules de classe affichés dans la zone **Modules** du volet de navigation pour la fonction spécifiée par l'argument **Nom fonction**.</span><span class="sxs-lookup"><span data-stu-id="5068d-p104">If you use the **RunCode** action to call a function, Access looks for the function with the name specified by the **Function Name** argument in the standard modules for the database. However, when this action runs in response to clicking a menu command on a form or report or in response to an event on a form or report, Access first looks for the function in the form's or report's class module and then in the standard modules. Access doesn't search the class modules that appear in the **Modules** area of the Navigation Pane for the function specified by the **Function Name** argument.</span></span>

<span data-ttu-id="5068d-p105">Cette action n'est pas disponible dans un module VBA. À la place, exécutez la procédure Function requise directement dans VBA.</span><span class="sxs-lookup"><span data-stu-id="5068d-p105">This action isn't available in a VBA module. Instead, run the desired Function procedure directly in VBA.</span></span>

