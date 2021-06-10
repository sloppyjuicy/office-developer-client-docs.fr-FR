---
title: Database.NewPassword, méthode (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294854"
---
# <a name="databasenewpassword-method-dao"></a>Database.NewPassword, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Permet de modifier le mot de passe d’une base de données existante du moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* NewPassword(***bstrOld***, ***bstrNew***)

*expression* Expression qui renvoie un objet **Database.**

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>bstrOld</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Définition actuelle de la propriété <strong>Password</strong> de l'objet <strong>Database</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>bstrNew</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Nouveau paramètre de la propriété <strong>Password</strong> de l’objet <strong>Database.</strong></p>
<p><strong>REMARQUE</strong>: utilisez des mots de passe forts qui combinent des lettres majuscules et minuscules, des chiffres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort facile à mémoriser afin de ne pas avoir à le noter.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Les chaînes bstrOld et bstrNew peuvent comporter jusqu’à 20 caractères et inclure tous les caractères à l’exception du caractère ASCII 0 (null). Pour effacer le mot de passe, utilisez une chaîne de longueur nulle («  ») pour bstrNew.

Les mots de passe respectent la casse.

Si une base de données n'est associée à aucun mot de passe, le moteur de base de données Microsoft Access en crée un automatiquement en transmettant une chaîne vide ("") pour l'ancien mot de passe.


> [!IMPORTANT]
> [!IMPORTANTE] Si vous perdez votre mot de passe, vous ne pourrez plus jamais ouvrir la base de données.


