---
title: OpenVisualBasicModule, action de macro
TOCTitle: OpenVisualBasicModule macro action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7d3d2d5f76e087e428bc9211805c524ebe5247d9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930447"
---
# <a name="openvisualbasicmodule-macro-action"></a>OpenVisualBasicModule, action de macro


**S’applique à**: Access 2013, Office 2013

Utilisez l'action **OuvrirModuleVisualBasic** pour ouvrir un module Visual Basic pour Applications (VBA) spécifique à une certaine procédure. Il peut s'agir d'une procédure Sub, d'une procédure Function ou d'une procédure événementielle.


> [!NOTE]
> <P>[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</P>



## <a name="setting"></a>Paramètre

L'action **OuvrirModuleVisualBasic** utilise les arguments suivants :

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
<td><p><strong>Nom du module</strong></p></td>
<td><p>Le nom du module que vous souhaitez ouvrir. Vous pouvez laisser cet argument vide si vous souhaitez rechercher tous les modules standard dans la base de données pour une procédure et ouvrez le module approprié dans cette procédure. Si vous exécutez une macro contenant l’action <strong>OuvrirModuleVisualBasic</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord le module portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de la procédure</strong></p></td>
<td><p>Nom de la procédure dans laquelle vous voulez ouvrir le module. Si vous laissez cet argument vierge, le module s’ouvre sur la section Déclarations.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!REMARQUE] Vous devez entrer un nom valide dans l'argument <STRONG>Nom du module</STRONG> ou <STRONG>Nom de la procédure</STRONG>.</P>



## <a name="remarks"></a>Notes

Vous pouvez utiliser cette action pour ouvrir une procédure événementielle en spécifiant les arguments **Nom du module** et **Nom de la procédure**. Par exemple, pour ouvrir la procédure d’événement **Click** du bouton ImpressionFacture du formulaire commandes, définissez l’argument **Nom du Module** sur **formulaire.commandes** et définissez l’argument **Nom de la procédure** à **ImprimerFacture\_cliquez sur**. Pour afficher la procédure événementielle d'un formulaire ou d'un état, celui-ci doit être ouvert.

De même, pour ouvrir une procédure dans un module de classe, vous devez spécifier le nom du module, bien que celui-ci ne doit pas être ouvert.

Pour ouvrir une procédure privée, le module qui la contient doit être ouvert.

Cette action revient à cliquer avec le bouton droit sur un module dans le volet de navigation et à cliquer ensuite sur **Mode Création**. Cette action vous permet également de spécifier un nom de procédure et de rechercher les modules standard dans une base de données de procédures.


> [!TIP]
> <P>[!CONSEIL] Vous pouvez sélectionner un module dans le volet de navigation et le faire glisser vers une ligne d'action de macro. Ceci crée automatiquement une action <STRONG>OuvrirModuleVisualBasic</STRONG> qui ouvre le module dans la section Déclarations.</P>



Pour exécuter l'action **OuvrirModuleVisualBasic** dans un module VBA, utilisez la méthode **OpenModule** de l'objet **DoCmd**.

