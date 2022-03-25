---
title: Recordset.RecordsetType, propriété (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 03/22/2022
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 72b34ce7c0ad21bf572992ec0f3d68a0dd3dcb9c
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63723410"
---
# <a name="recordsetrecordsettype-property-dao"></a>Recordset.RecordsetType, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

La propriété **RecordsetType** permet de spécifier le genre de jeu d'enregistrement disponible pour un formulaire. Type de données **Byte** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*.* RecordsetType

*expression* Variable qui représente un objet **Form**.

## <a name="remarks"></a>Remarques

La propriété **RecordsetType** utilise les paramètres suivants dans une base de données Microsoft Access.

|**Paramètre**|**Type de jeu d'enregistrement**|**Description**|
|:----------|:--------------------|:--------------|
| 0 | Feuille deynaset (par défaut)  | Vous pouvez modifier des contrôles liés basés sur une ou plusieurs tables avec une relation un-à-un. Pour les contrôles liés à des champs basés sur des tables avec une relation un-à-plusieurs, &quot;&quot; vous ne pouvez pas modifier les données du champ joint du côté un de la relation, sauf si la mise à jour en cascade est activée entre les tables.</br>|
| 1 | Feuille rép.dyn.(MAJ globale) | Toutes les tables et tous les contrôles correspondant à leurs champs peuvent être édités.</br>|
| 2| Capture instantanée | Aucune table ou aucun contrôle correspondant à leurs champs ne peut être édité.</br>|

> [!NOTE]
> [!REMARQUE] Si vous ne voulez pas que les données des contrôles dépendants soient modifiées quand un formulaire est en mode Formulaire ou en mode Feuille de données, vous pouvez définir la propriété **RecordsetType** sur 2.

Dans un projet Microsoft Access (.adp), la propriété **RecordsetType** utilise les paramètres suivants :

|**Paramètre**|**Type de jeu d'enregistrement**|**Description**|
|:----------|:--------------------|:--------------|
| 3 | Capture instantanée | Aucune table ou aucun contrôle correspondant à leurs champs ne peut être édité.</br>|
| 4 | Possibilité de mise à jour de l'instantané | (Valeur par défaut) Toutes les tables et tous les contrôles correspondant à leurs champs peuvent être édités.</br>|

> [!NOTE]
> [!REMARQUE] Toute modification de la propriété **RecordsetType** d'un état ou d'un formulaire ouvert entraîne la recréation automatique d'un jeu d'enregistrements.

Vous pouvez créer des formulaires basés sur des tables sous-jacentes multiples avec des champs correspondants à des contrôles dans les formulaires. En fonction du paramètre de la propriété **RecordsetType**, vous pouvez choisir lesquels de ces contrôles dépendants pourront être édités.

Outre le contrôle d’édition fourni par **RecordsetType**, chaque contrôle d’un formulaire possède une propriété **Locked** que vous pouvez définir pour spécifier si le contrôle et ses données sous-jacentes peuvent être modifiés. Si la propriété **Locked** est définie sur Oui, vous ne pouvez pas modifier les données.

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

- [Form, objet](/office/vba/api/Access.Form.md)
