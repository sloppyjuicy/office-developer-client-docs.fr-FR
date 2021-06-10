---
title: Recordset2.Update, méthode (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307167"
---
# <a name="recordset2update-method-dao"></a>Recordset2.Update, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* .Update(***UpdateType***, ***Force***)

*expression* Variable qui représente un **objet Recordset2.**

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
<td><p><em>UpdateType</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>A <strong> <a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a> </strong> constante indiquant le type de mise à jour, comme spécifié dans les paramètres (espaces).</p></td>
</tr>
<tr class="even">
<td><p><em>Force</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p>A <strong>booléenne</strong> valeur indiquant forcer les modifications dans la base de données quelle que soit la si les données sous-jacentes a été modifiées par un autre utilisateur depuis ou non le <strong> <a href="recordset-addnew-method-dao.md">AddNew</a> </strong>, <strong> <a href="fields-delete-method-dao.md">Supprimer</a></strong>, ou <strong> <a href="recordset2-edit-method-dao.md">modifier</a> </strong> appeler. Si <strong>vrai</strong>, les modifications sont forcées et les modifications apportées par d’autres utilisateurs sont simplement remplacées. Si <strong>faux</strong> (par défaut), les modifications apportées par un autre utilisateur alors que la mise à jour est en attente entraînera la mise à jour Échec pour ces modifications sont en conflit. Aucune erreur se produit, mais le <strong> <a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a> </strong> et  <strong>BatchCollisions</strong>  propriétés indique le nombre des conflits et les lignes concernées par conflits, respectivement (espaces).</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez **mise à jour** pour enregistrer l’enregistrement actif et toutes les modifications apportées à celui-ci.

> [!IMPORTANT]
> Enregistrer les modifications apportées à l’enregistrement actif
> - Vous utilisez le **modifier** ou **AddNew** méthode, puis accéder à un autre enregistrement sans utiliser première **mise à jour**.
> - Vous utilisez **modifier** ou **AddNew**, puis utilisez **modifier** ou **AddNew** nouveau sans utiliser première **mise à jour**.
> - Vous définissez la **[signet](recordset2-bookmark-property-dao.md)** propriété vers un autre enregistrement.
> - Vous fermez le **jeu d’enregistrements** sans utiliser première **mise à jour**.
> - Vous annulez la **modifier** opération à l’aide **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.

Pour modifier un enregistrement, utilisez la **modifier** méthode pour copier le contenu de l’enregistrement actif dans la mémoire tampon de copie. Si vous n’utilisez **modifier** tout d’abord, une erreur se produit lorsque vous utilisez **mise à jour** ou tenter de modifier la valeur du champ.

Dans un espace de travail ODBCDirect, vous pouvez effectuer par lot mises à jour, sous réserve la bibliothèque curseur prend en charge les mises à jour du lot et le **jeu d’enregistrements** a été ouvert avec l’option de verrouillage par lot optimiste.

Dans un espace de travail Microsoft Access, lorsque le **jeu d’enregistrements** d’objet **LockEdits** paramètre de la propriété est **vrai** (verrouillage pessimiste) dans un environnement multi-utilisateurs, l’enregistrement reste verrouillé à partir du moment **modifier** sert jusqu'à ce que le **mise à jour** méthode est exécutée ou la modification est annulée. Si le **LockEdits** paramètre de la propriété est **faux** (verrouillage optimiste), l’enregistrement est verrouillé et par rapport à l’enregistrement déjà modifiée juste avant qu’il est mis à jour dans la base de données. Si l’enregistrement a changé, car vous avez utilisé le **modifier** méthode, le **mise à jour** opération échoue. Base de données Microsoft Access connectées moteur ODBC et bases de données ISAM toujours utilisent le verrouillage optimiste. Pour continuer la **mise à jour** opération avec vos modifications, utilisez la **mise à jour** méthode nouveau. Pour revenir à l’enregistrement tel que l’autre utilisateur l’a modifié, actualisez l’enregistrement actif à l’aide de la commande Move 0.

> [!NOTE]
> Pour ajouter, modifier ou supprimer un enregistrement, il doit y avoir un index unique sur l’enregistrement dans la source de données sous-jacentes. Si non, une erreur « Autorisation refusée » doit se produire sur le **AddNew**, **supprimer**, ou **modifier** méthode appel dans un espace de travail Microsoft Access ou une erreur « Argument non valide » se produit sur la **mise à jour** appeler dans un espace de travail ODBCDirect.


