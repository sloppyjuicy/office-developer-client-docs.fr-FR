---
title: Méthode Recordset2.Update (DAO)
TOCTitle: Update Method
ms:assetid: 1b47606a-e79c-23f1-b120-46d1429bc167
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845700(v=office.15)
ms:contentKeyID: 48543537
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052882
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4259da0eb48e7ff13e246b326cc6e96d7a916ea7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714912"
---
# <a name="recordset2update-method-dao"></a>Méthode Recordset2.Update (DAO)

**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . Mise à jour (***UpdateType***, ***Force***)

*expression* Variable qui représente un objet **Recordset2** .

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
<th><p>Nom</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>UpdateType</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> qui indique le type de mise à jour, comme spécifié dans les paramètres (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><em>Force</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p>Valeur <strong>booléenne</strong> indiquant si les modifications doivent être forcées ou non dans la base de données, indépendamment du fait que les données sous-jacentes aient été modifiées par un autre utilisateur depuis l'appel de <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> ou <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong>. Si la valeur est <strong>True</strong>, les modifications sont forcées et les modifications apportées par d'autres utilisateurs sont tout simplement remplacées. Si la valeur est <strong>False</strong> (valeur par défaut), les modifications apportées par d'autres utilisateurs tandis que la mise à jour est en attente entraîneront l'échec de la mise à jour pour les modifications en conflit. Aucune erreur ne se produit, mais les propriétés <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> et <strong>BatchCollisions</strong> indiqueront le nombre de conflits et les lignes concernées par ces conflits, respectivement (espaces de travail ODBCDirect uniquement).  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez la méthode **Update** pour enregistrer l'enregistrement actif et les modifications que vous y avez effectuées.

> [!IMPORTANT]
> [!IMPORTANTE] Les modifications apportées à l'enregistrement actif sont perdues dans les cas suivants :
> - vous utilisez la méthode **Edit** ou **AddNew** et passez à un autre enregistrement sans utiliser au préalable la méthode **Update**;
> - vous utilisez la méthode **Edit** ou **AddNew**, puis vous réutilisez la méthode **Edit** ou **AddNew** sans utiliser au préalable la méthode **Update**
> - vous affectez la propriété **[Bookmark](recordset2-bookmark-property-dao.md)** à un autre enregistrement ;
> - vous fermez l'objet **Recordset** sans utiliser au préalable la méthode **Update**;
> - vous annulez l'opération **Edit** par le biais de la méthode **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.

Pour modifier un enregistrement, utilisez la méthode **Edit** pour copier le contenu de l'enregistrement actif dans la mémoire tampon de la copie. Si vous n'utilisez pas d'abord la méthode **Edit**, une erreur se produit lorsque vous utilisez **Update** ou que vous tentez de modifier la valeur d'un champ.

Dans un espace de travail ODBCDirect, vous pouvez effectuer des mises à jour par lot, à condition que la bibliothèque de curseurs prenne en charge ce type d'opération et que l'objet **Recordset** ait été ouvert avec l'option de verrouillage par lot optimiste.

Dans un espace de travail Microsoft Access, lorsque la propriété **LockEdits** de l'objet **Recordset** a la valeur **True** (verrouillage pessimiste) dans un environnement multi-utilisateur, l'enregistrement reste verrouillé du moment où la méthode **Edit** est utilisée jusqu'à l'exécution de la méthode **Update** ou l'annulation de la modification. Si la propriété **LockEdits** a la valeur **False** (verrouillage optimiste), l'enregistrement est verrouillé et comparé à l'enregistrement tel qu'il était avant sa modification juste avant sa mise à jour dans la base de données. Si l'enregistrement a changé depuis l'utilisation de la méthode **Edit**, l'opération **Update** échoue. Les bases de données ODBC et ISAM installables connectées au moteur de base de données Microsoft Access utilisent toujours un verrouillage optimiste. Pour poursuivre l'opération **Update** avec vos modifications, utilisez à nouveau la méthode **Update**. Pour revenir à l’enregistrement en tant que l’autre utilisateur l’avait modifié, actualisez l’enregistrement actif en utilisant Move 0.

> [!NOTE]
> [!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, un index unique doit exister au niveau de l'enregistrement de la source de données sous-jacente. À défaut, une erreur de type « Autorisation refusée » se produit consécutivement à l'appel d'une méthode **Update**, **Edit** ou **AddNew** dans un espace de travail Microsoft Access ; dans un espace de travail ODBCDirect, l'appel de **Delete** provoque une erreur de type « Argument incorrect ».


