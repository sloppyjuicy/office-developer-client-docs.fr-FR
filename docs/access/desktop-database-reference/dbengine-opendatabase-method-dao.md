---
title: DBEngine.OpenDatabase, méthode (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1cd4188931999284a6454064a0906b64cf1f519a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294252"
---
# <a name="dbengineopendatabase-method-dao"></a>DBEngine.OpenDatabase, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Ouvre une base de données spécifiée et renvoie une référence à l’objet **[Database](database-object-dao.md)** qui le représente.

## <a name="syntax"></a>Syntaxe

*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

*expression* Variable représentant un objet **DBEngine**.

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
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Nom d'un fichier de base de données Microsoft Access existant ou nom de source de données (DSN) d'une source de données ODBC. Consultez la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour obtenir plus d'informations sur la définition de cette valeur.  </p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Définit différentes options pour la base de données, selon les indications dans les notes.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> si vous souhaitez ouvrir la base de données avec un accès en lecture seule, ou <strong>False</strong> (valeur par défaut) si vous souhaitez ouvrir la base de données avec un accès en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Spécifie les différentes informations de connexion, dont les mots de passe.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Database

## <a name="remarks"></a>Remarques

Vous pouvez utiliser les valeurs ci-dessous pour l’argument options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Setting</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>True</strong></p></td>
<td><p>Ouvre la base de données en mode exclusif.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(Valeur par défaut) Ouvre la base de données en mode partagé.</p></td>
</tr>
</tbody>
</table>


Lorsque vous ouvrez une base de données, elle est automatiquement ajoutée à la collection **Databases**.

Certaines considérations s’appliquent lorsque vous utilisez dbname :

- S'il s'agit d'une base de données déjà ouverte pour un accès par un autre utilisateur, une erreur se produit.

- S'il ne s'agit pas d'une base de données existante ou d'un nom de source de données ODBC valide, une erreur se produit.

- S’il s’agit d’une chaîne nulle ("") et si *connect* prend la valeur "ODBC;", une boîte de dialogue répertoriant tous les noms de source de données ODBC enregistrés s’affiche afin que l’utilisateur puisse sélectionner une base de données.

Pour fermer une base de données, et ainsi supprimer l’objet **Database** de la collection **Databases**, utilisez la méthode **[Close](connection-close-method-dao.md)** dans l’objet.

> [!NOTE]
> Lorsque vous accédez à une source de données ODBC connectée au moteur de base de données Microsoft Access, vous pouvez améliorer les performances de votre application en ouvrant un objet **Database** connecté à la source de données ODBC, ce qui vous évite de lier des objets [TableDef](tabledef-object-dao.md) individuels à des tables spécifiques dans la source de données ODBC.


