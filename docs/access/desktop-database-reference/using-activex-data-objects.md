---
title: Utilisation d’ActiveX Data Objects (ADO)
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access fournit trois modèles objet à utiliser dans la création, la maintenance et la gestion de vos bases de données Access et de leurs données associées à l’aide de Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 954ab4cd2922eb02ff0bda7a61ab5e4b4e91257a
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631922"
---
# <a name="use-activex-data-objects"></a>Utilisation d’ActiveX Data Objects (ADO)

**S’applique à** : Access 2013, Office 2013

Microsoft Access fournit trois modèles objet à utiliser dans la création, la maintenance et la gestion de vos bases de données Access et de leurs données associées à l’aide de Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Objets de données Microsoft ActiveX (ADO)

ADO contient les objets nécessaires pour créer, maintenir et supprimer des enregistrements dans une source de données.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO ext. pour DDL et sécurité (ADOX)

ADOX fournit les objets DDL (Data Definition Language) nécessaires pour créer une base de données et ses objets contenus en plus des objets nécessaires à la gestion de la sécurité.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Bibliothèque Microsoft Jet and Replication Objects 2.5 (JRO)

Étant donné que les objets ADO ont été conçus pour fonctionner avec de nombreuses bases de données en plus des bases de données Microsoft Jet, les fonctionnalités propres à Jet ont été décomposées dans la bibliothèque JRO.

Le tableau ci-dessous indique les fonctionnalités offertes par chaque composant par rapport à DAO.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Les fonctionnalités</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(MDBs uniquement)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Créez des jeux d’enregistrements.</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés de démarrage.</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Prise en charge d’ANSI92 SQL.***</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Créez des tableaux.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créez une base de données.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés d’un tableau existant.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créez des relations de tableau.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les paramètres de sécurité.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Prise en charge de l’attribut Compression pour les données de colonne.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier des requêtes ou des affichages SQL de base stockés.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer des requêtes permanentes uniquement accessibles par code</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Créer des requêtes accessibles par conteneur/IU et code de base de données</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Compacter/coder la base de données.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Actualiser le cache.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Rendre la base de données réplicable.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Effectuer des réplicas de base de données.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Synchroniser les réplicas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés de la base de données.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer des propriétés de base de données personnalisées.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés des colonnes de tableau.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

\* Uniquement disponible pour la manipulation de bases de données Microsoft Access. Les versions futures de SQL Provider offriront peut-être cette fonctionnalité dans des projets Microsoft Access (.adp).

\*\* Uniquement disponible pour la manipulation de projets Access.

\*\*\*Bien que le moteur de base de données Access prend en charge certains SQL ANSI 92, il n’est pas encore entièrement conforme ANSI92.

1 Utilise un **objet Connection** pour référencer la base de données.

2 Utilise un **objet Catalog** pour référencer la base de données.

3 Utilise un **objet Replica** pour référencer la base de données.

4 Utilise un **objet JetEngine** pour référencer la base de données.

> [!NOTE]
> Contrairement à DAO, les objets ADO et ADOX peuvent effectuer les actions marquées dans des bases de données autres que Jet tant que le fournisseur de ces bases de données prend en charge cette action.
