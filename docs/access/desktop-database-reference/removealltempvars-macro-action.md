---
title: RemoveAllTempVars, action de macro
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: eade809a6e3982dc0dc4cf94ae382af72e8f454e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306796"
---
# <a name="removealltempvars-macro-action"></a><span data-ttu-id="61bc4-102">RemoveAllTempVars, action de macro</span><span class="sxs-lookup"><span data-stu-id="61bc4-102">RemoveAllTempVars macro action</span></span>


<span data-ttu-id="61bc4-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61bc4-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="61bc4-104">L’action **SupprimerToutesVarTemp** permet de supprimer toutes les variables temporaires que vous avez créées en utilisant l’action **DéfinirVarTemp**.</span><span class="sxs-lookup"><span data-stu-id="61bc4-104">You can use the **RemoveAllTempVars** action to remove any temporary variables that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="61bc4-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="61bc4-105">Setting</span></span>

<span data-ttu-id="61bc4-106">L’action **SupprimerToutesVarTemp** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="61bc4-106">The **RemoveAllTempVars** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="61bc4-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="61bc4-107">Remarks</span></span>

  - <span data-ttu-id="61bc4-p101">Vous pouvez définir jusqu'à 255 variables temporaires à la fois. Toute variable temporaire non supprimée reste en mémoire jusqu'à ce que la base de données ou le projet soit fermé. Il est conseillé de supprimer les variables temporaires lorsque vous ne les utilisez plus.</span><span class="sxs-lookup"><span data-stu-id="61bc4-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database or project. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="61bc4-111">Access supprime automatiquement toutes les variables temporaires lorsque vous fermez la base de données ou le projet.</span><span class="sxs-lookup"><span data-stu-id="61bc4-111">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="61bc4-112">Pour supprimer une seule variable temporaire, utilisez l'action **SupprimerVarTemp** et définissez son argument sur le nom de la variable temporaire que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="61bc4-112">To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.</span></span>

  - <span data-ttu-id="61bc4-113">Pour exécuter l'action **SupprimerToutesVarTemp** dans un module VBA, utilisez la méthode **RemoveAll** de l'objet **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="61bc4-113">To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="61bc4-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="61bc4-114">Example</span></span>

<span data-ttu-id="61bc4-115">La macro suivante illustre comment créer une variable temporaire, l'utiliser dans une condition et une zone de message, puis la supprimer en utilisant l'action **SupprimerToutesVarTemp**.</span><span class="sxs-lookup"><span data-stu-id="61bc4-115">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61bc4-116">Condition</span><span class="sxs-lookup"><span data-stu-id="61bc4-116">Condition</span></span></p></th>
<th><p><span data-ttu-id="61bc4-117">Action</span><span class="sxs-lookup"><span data-stu-id="61bc4-117">Action</span></span></p></th>
<th><p><span data-ttu-id="61bc4-118">Arguments</span><span class="sxs-lookup"><span data-stu-id="61bc4-118">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="61bc4-119"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="61bc4-119"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="61bc4-120"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox( &quot; Enter a non-zero number. &quot; )</span><span class="sxs-lookup"><span data-stu-id="61bc4-120"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61bc4-121">[TempVars]![MaVar] &lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="61bc4-121">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="61bc4-122"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="61bc4-122"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="61bc4-123"><strong>Message</strong>: = &quot; vous avez entré &quot; &amp; [TempVars]![ MyVar] &amp; &quot; . &quot; <strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span><span class="sxs-lookup"><span data-stu-id="61bc4-123"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="61bc4-124"><strong>RemoveAllTempVars</strong></span><span class="sxs-lookup"><span data-stu-id="61bc4-124"><strong>RemoveAllTempVars</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

