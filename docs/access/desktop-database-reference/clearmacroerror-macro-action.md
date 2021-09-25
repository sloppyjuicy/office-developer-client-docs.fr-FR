---
title: ClearMacroError, action de macro
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 675b8926d69b7cb5f52ed299d85d05dcd9cd82b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553206"
---
# <a name="clearmacroerror-macro-action"></a>ClearMacroError, action de macro


**S’applique à** : Access 2013, Office 2013


Utilisez l'action **EffacerMacroErreur** pour effacer les informations sur une erreur qui sont stockées dans l'objet **MacroError**.

## <a name="setting"></a>Paramètre

L’action **EffacerMacroErreur** ne possède aucun argument.

## <a name="remarks"></a>Remarques

- Lorsqu'une erreur se produit dans une macro, les informations sur l'erreur sont stockées dans l'objet **MacroError**. Si vous n’avez pas utilisé l’action **[SurErreur](onerror-macro-action.md)** pour supprimer les messages d’erreur, la macro s’arrête et les informations d’erreur s’affichent dans un message d’erreur standard. Toutefois, si vous avez utilisé l’action **SurErreur** pour supprimer les messages d’erreur, vous pouvez utiliser les informations stockées dans l’objet **MacroError** dans une condition ou dans un message d’erreur personnalisé.
    
  Lorsqu'une erreur a été gérée, les informations stockées dans l'objet **MacroError** deviennent obsolètes. Il est alors conseillé d'effacer l'objet à l'aide de l'action **EffacerMacroErreur**, ce qui permet de réinitialiser à 0 le numéro d'erreur dans l'objet **MacroError** et de supprimer toutes les autres informations sur l'erreur, telles que sa description, le nom de la macro, ainsi que le nom, la condition et les arguments de l'action. Ainsi, vous pourrez réexaminer ultérieurement l'objet **MacroError** pour déterminer si une autre erreur s'est produite.

- L'objet **MacroError** est automatiquement effacé à l'issue d'une macro. Il n'est donc pas nécessaire d'utiliser l'action **EffacerMacroErreur** à la fin d'une macro.

- L'objet **MacroError** ne contient des informations que sur une seule erreur à la fois. Si plusieurs erreurs se sont produites dans une macro, l'objet **MacroError** ne contient des informations que sur la dernière erreur.

- Pour exécuter l'action **EffacerMacroErreur** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **ClearMacroError** de l'objet **DoCmd**.

## <a name="example"></a>Exemple

La macro suivante utilise l'action **SurErreur** avec l'argument **Suivant** pour supprimer les messages d'erreur, puis utilise l'action **OuvrirFormulaire** pour ouvrir un formulaire. Pour les besoins de cet exemple, une erreur a été délibérément créée en utilisant l'action **AtteindreEnregistrement** pour revenir à l'enregistrement précédent. La condition **\[ MacroError \] . \[ La \] \<\> numéro 0** teste **l’objet MacroError.** Si une erreur s'est produite, le numéro de l'erreur est une valeur non nulle et l'action **ZoneMessage** s'exécute. La zone de message affiche le nom de l'action à l'origine de l'erreur (dans le cas présent, l'action **AtteindreEnregistrement** ) et le numéro de l'erreur est affiché. Pour finir, l’action **EffacerMacroErreur** est exécutée afin d’effacer l’objet **MacroError**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Action</p></th>
<th><p>Arguments</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OnError</strong></p></td>
<td><p><strong>Atteindre</strong> : <strong>Suivant</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nom du</strong>formulaire :<strong>CategoryForm View</strong>: <strong>Mode FormWindow</strong>: <strong>Normal</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>Type d’objet</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</p></td>
</tr>
<tr class="even">
<td><p>[MacroError]. [Number] &lt; &gt; 0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: = &quot; Error # &quot; &amp; [MacroError].[ Number] &amp; &quot; on &quot; &amp; [MacroError].[ ActionName]. &amp; &quot; &quot; <strong>Beep</strong>: <strong>YesType</strong>: Information</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

