---
title: Méthode DBEngine.OpenDatabase (DAO)
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
ms.openlocfilehash: 6999c003883675837ad333b6488820f3bb3a9f2e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472224"
---
# <a name="dbengineopendatabase-method-dao"></a>Méthode DBEngine.OpenDatabase (DAO)


**S’applique à**: Access 2013 | Office 2013

Ouvre une base de données spécifiée et renvoie une référence à l'objet **[Database](database-object-dao.md)** qui la représente.

## <a name="syntax"></a>Syntaxe

*expression* . OpenDatabase (***nom***, ***Options***, ***ReadOnly***, ***connecter***)

*expression* Variable qui représente un objet **DBEngine** .

### <a name="parameters"></a>Paramètres

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
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Nom d'un fichier de base de données Microsoft Access existant ou nom de source de données (DSN) d'une source de données ODBC. Consultez la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour obtenir plus d'informations sur la définition de cette valeur.  </p></td>
</tr>
<tr class="even">
<td><p>Options</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Définit différentes options pour la base de données, selon les indications dans les notes.</p></td>
</tr>
<tr class="odd">
<td><p>ReadOnly</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p><strong>True</strong> si vous souhaitez ouvrir la base de données avec un accès en lecture seule, ou <strong>False</strong> (valeur par défaut) si vous souhaitez ouvrir la base de données avec un accès en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p>Connexion</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Spécifie les différentes informations de connexion, dont les mots de passe.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Base de données

## <a name="remarks"></a>Remarques

Vous pouvez utiliser les valeurs ci-dessous pour l'argument options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Paramètre</p></th>
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

Certaines considérations s’appliquent lorsque vous utilisez NomBaseDonnées :

  - S'il s'agit d'une base de données déjà ouverte pour un accès par un autre utilisateur, une erreur se produit.

  - S'il ne s'agit pas d'une base de données existante ou d'un nom de source de données ODBC valide, une erreur se produit.

  - S’il s’agit d’une chaîne de longueur nulle (« ») et *vous connecter* est « ODBC ; », une boîte de dialogue répertoriant les noms de source de données ODBC tous enregistrés s’affiche afin que l’utilisateur peut sélectionner une base de données.

Pour fermer une base de données et ainsi supprimer l'objet **Database** de la collection **Databases**, utilisez la méthode **[Close](connection-close-method-dao.md)** sur l'objet.


> [!NOTE]
> <P>[!REMARQUE] Lorsque vous accédez à une source de données ODBC connectée au moteur de base de données Microsoft Access, vous pouvez améliorer les performances de votre application en ouvrant un objet <STRONG>Database</STRONG> connecté à la source de données ODBC, ce qui vous évite de lier des objets <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> individuels à des tables spécifiques dans la source de données ODBC.</P>


