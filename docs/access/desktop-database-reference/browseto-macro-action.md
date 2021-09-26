---
title: BrowseTo, action de macro
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 53cc7fd0b085efee9b52d53371b08e338ccd4665
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607079"
---
# <a name="browseto-macro-action"></a>BrowseTo, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l'action **Parcourir** pour naviguer parmi des objets en place. Vous pouvez également modifier l'objet source d'un contrôle de sous-formulaire en spécifiant l'argument Chemin d'accès au contrôle de sous-formulaire. Utilisez **Parcourir** pour naviguer de formulaire1 à formulaire2 sans ouvrir de nouvelle fenêtre.

## <a name="setting"></a>Paramètre

L’action **Parcourir** utilise l’argument suivant :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Type d’objet</p></td>
<td><p>Type d’objet vers lequel naviguer.</p></td>
</tr>
<tr class="even">
<td><p>Nom de l’objet</p></td>
<td><p>Objet qui se charge à l’intérieur du contrôle de sous-formulaire référencé par l’argument Chemin d’accès au contrôle de sous-formulaire.</p></td>
</tr>
<tr class="odd">
<td><p>Chemin d’accès au contrôle de sous-formulaire</p></td>
<td><p>S’il est spécifié, le chemin d’accès du formulaire principal de l’application au contrôle de sous-formulaire cible qui charge l’objet spécifié par l’argument Nom de l’objet.</p></td>
</tr>
<tr class="even">
<td><p>Condition Where</p></td>
<td><p>Si spécifié, remplace la condition WHERE de la source d’enregistrement de l’objet.</p></td>
</tr>
<tr class="odd">
<td><p>Page</p></td>
<td><p>Spécifié, définit la page du formulaire continu qui deviendra la page active. Cet argument est web uniquement.</p></td>
</tr>
<tr class="even">
<td><p>Mode Données</p></td>
<td><p>Si spécifié, il s’agit du mode de saisie des données du formulaire.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'argument Chemin d'accès au contrôle de sous-formulaire doit être spécifié à l'aide de la syntaxe de l'exemple de code suivant :

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

Dans cet exemple, le Formulaire principal est le formulaire de niveau supérieur dans l'application cliente Access. L'argument Chemin d'accès au contrôle de sous-formulaire doit spécifier en alternance les noms des contrôles de sous-formulaire et formulaire menant du formulaire principal au contrôle de sous-formulaire qui est le conteneur de l'objet spécifié par l'argument Nom d'objet. Chaque contrôle de sous-formulaire spécifié doit être un contrôle sur le formulaire qui le précède. Le chemin d'accès doit se terminer par un contrôle de sous-formulaire.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser l’action Parcourir pour ouvrir un état dans un contrôle de sous-forme ou dans un contrôle de navigation.

**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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



