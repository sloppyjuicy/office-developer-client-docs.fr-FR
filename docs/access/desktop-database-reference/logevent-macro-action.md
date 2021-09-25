---
title: LogEvent, action de macro
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5868f8c351bfacba2008b114f5df1596eb4a246f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602254"
---
# <a name="logevent-macro-action"></a>LogEvent, action de macro

**S’applique à** : Access 2013, Office 2013

L'action **ConsignerÉvénement** écrit des informations dans la table système **USysApplicationLog**.

> [!NOTE]
> L’action **USysApplicationLog** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Paramètre

L’action **ConsignerÉvénement** utilise les arguments suivants.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Obligatoire</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Description</strong></p></td>
<td><p>Non</p></td>
<td><p>Expression de type Chaîne qui décrit la condition que vous souhaitez consigner. La description ne doit pas dépasser 255 caractères.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

L'action **ConsignerÉvénement** peut être utilisée pour écrire des informations d'état dans la table système **USysApplicationLog** qui ne méritent pas l'utilisation de l'action **[DéclencherErreur](raiseerror-macro-action.md)** pour lever une erreur. Par exemple, vous pouvez consigner les modifications apportées à un champ spécifique ou utiliser les éléments écrits dans **USysApplicationLog** pour vous aider à déboguer votre macro.

Lorsque vous utilisez l'action **ConsignerÉvénement** pour écrire dans la table **USysApplicationLog**, la colonne **Catégorie** prend automatiquement la valeur **Utilisateur**.

Pour afficher la table **USysApplicationLog**, procédez comme suit :

1.  Cliquez sur le menu **Fichier**, puis cliquez sur **Options**.

2.  Dans la boîte dialogue **Options Access**, cliquez sur l'onglet **Base de données active**.

3.  Dans la section **Navigation**, cliquez sur **Options de navigation**.

4.  Dans la boîte de dialogue **Options de navigation**, cliquez sur **Afficher les objets système**, puis sur **OK**.

5.  Cliquez sur **OK** pour fermer la boîte de dialogue **Options Access**.

