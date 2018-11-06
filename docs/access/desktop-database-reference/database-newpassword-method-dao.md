---
title: Méthode Database.NewPassword (DAO)
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
ms.openlocfilehash: e72d879482c3ed69b262f2f4d0f07a4e11f8fa4c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998937"
---
# <a name="databasenewpassword-method-dao"></a>Méthode Database.NewPassword (DAO)

**S’applique à**: Access 2013, Office 2013

Permet de modifier le mot de passe d'une base de données existante du moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . NewPassword (***chaînes bstrAncien***, ***bstrNouveau***)

*expression* Expression qui renvoie un objet de **base de données** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>chaînes bstrAncien</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Définition actuelle de la propriété <strong>Password</strong> de l'objet <strong>Database</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>bstrNouveau</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Le nouveau paramètre de la propriété de <strong>mot de passe</strong> de l’objet de <strong>base de données</strong> .</p>
<p><strong>Remarque</strong>: utilisez des mots de passe forts combinant des majuscules et minuscules, nombres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Les chaînes bstrAncien et bstrNouveau peuvent comporter jusqu'à 20 caractères et peut comprendre des caractères, à l’exception du caractère ASCII 0 (null). Pour effacer le mot de passe, utilisez une chaîne de longueur nulle (" ») pour l’argument bstrNouveau.

Les mots de passe respectent la casse.

Si une base de données n'est associée à aucun mot de passe, le moteur de base de données Microsoft Access en crée un automatiquement en transmettant une chaîne vide ("") pour l'ancien mot de passe.


> [!IMPORTANT]
> [!IMPORTANTE] Si vous perdez votre mot de passe, vous ne pourrez plus jamais ouvrir la base de données.


