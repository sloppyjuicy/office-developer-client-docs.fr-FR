---
title: Propriété Recordset.RecordsetType (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e521c4de48f45d080a3b201ac431b2d7da14bc22
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923223"
---
# <a name="recordsetrecordsettype-property-dao"></a>Propriété Recordset.RecordsetType (DAO)

**S’applique à**: Access 2013, Office 2013

La propriété **RecordsetType** permet de spécifier le genre de jeu d'enregistrement disponible pour un formulaire. Type de données **Byte** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . RecordsetType

*expression* Une variable qui représente un objet **Form**.

## <a name="remarks"></a>Remarques

La propriété **RecordsetType** utilise les paramètres suivants dans une base de données Microsoft Access.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Paramètre</p></th>
<th><p>Type de jeu d'enregistrement</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>Feuille de réponse dynamique</p></td>
<td><p>(Valeur par défaut) Vous pouvez modifier les contrôles dépendants basés sur une seule table ou des tables avec une relation. Pour les contrôles liés à des champs basés sur des tables avec une relation un-à-plusieurs, vous ne pouvez pas modifier les données du champ sur la &quot;un&quot; côté de la relation, sauf si la mise à jour en cascade est activée entre les tables.</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>Feuille rép.dyn.(MAJ globale)</p></td>
<td><p>Toutes les tables et tous les contrôles correspondant à leurs champs peuvent être édités.</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>Instantané</p></td>
<td><p>Aucune table ou aucun contrôle correspondant à leurs champs ne peut être édité.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!REMARQUE] Si vous ne voulez pas que les données des contrôles dépendants soient modifiées quand un formulaire est en mode Formulaire ou en mode Feuille de données, vous pouvez définir la propriété **RecordsetType** sur 2.



Dans un projet Microsoft Access (.adp), la propriété **RecordsetType** utilise les paramètres suivants :

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Paramètre</p></th>
<th><p>Type de jeu d'enregistrement</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>3</p></td>
<td><p>Instantané</p></td>
<td><p>Aucune table ou aucun contrôle correspondant à leurs champs ne peut être édité.</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>Possibilité de mise à jour de l'instantané</p></td>
<td><p>(Valeur par défaut) Toutes les tables et tous les contrôles correspondant à leurs champs peuvent être édités.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!REMARQUE] Toute modification de la propriété **RecordsetType** d'un état ou d'un formulaire ouvert entraîne la recréation automatique d'un jeu d'enregistrements.



Vous pouvez créer des formulaires basés sur des tables sous-jacentes multiples avec des champs correspondants à des contrôles dans les formulaires. En fonction du paramètre de la propriété **RecordsetType**, vous pouvez choisir lesquels de ces contrôles dépendants pourront être édités.

Outre le contrôle d’édition fourni par la **propriété RecordsetType**, chaque contrôle d’un formulaire a une propriété **Locked** que vous pouvez définir pour spécifier si le contrôle et ses données sous-jacentes peuvent être modifiés. Si la propriété **Locked** est définie sur Oui, vous ne pouvez pas modifier les données.

## <a name="example"></a>Exemple

Dans l'exemple suivant, seul un utilisateur dont l'ID est ADMIN peut mettre à jour des enregistrements. Cet exemple de code définit la propriété **RecordsetType** sur Instantané si la valeur de la variable publique gstrUserID n'est pas ADMIN.

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a>Voir aussi

- [Form, objet](https://docs.microsoft.com/office/vba/api/Access.Form)


