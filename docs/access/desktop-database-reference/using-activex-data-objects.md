---
title: Utilisation d’ActiveX Data Objects (ADO)
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access propose trois modèles d'objet à utiliser pour la création, la maintenance et la gestion de vos bases de données Access et de leurs données liées à l'aide de Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312739"
---
# <a name="use-activex-data-objects"></a>Utilisation d’ActiveX Data Objects (ADO)

**S’applique à** : Access 2013, Office 2013

Microsoft Access propose trois modèles d'objet à utiliser pour la création, la maintenance et la gestion de vos bases de données Access et de leurs données liées à l'aide de Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Objets de données Microsoft ActiveX (ADO)

ADO contient les objets nécessaires pour créer, maintenir et supprimer des enregistrements dans une source de données.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO ext. for DDL and Security (ADOX)

ADOX fournit les objets DDL (Data Definition Language) nécessaires pour créer une nouvelle base de données et ses objets contenus en plus des objets nécessaires à la gestion de la sécurité.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Bibliothèque Microsoft Jet et rePlication Objects 2,5 (JRO)

Étant donné que les objets ADO ont été conçus pour fonctionner avec de nombreuses bases de données en plus des bases de données Microsoft Jet, les fonctionnalités propres à jet ont été décomposées dans la bibliothèque JRO.

Le tableau ci-dessous indique les fonctionnalités offertes par chaque composant par rapport à DAO.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fonctionnalité</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(MDB uniquement)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Créez des jeux d'enregistrements.</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés de démarrage.</p></td>
<td><p>X</p></td>
<td><p>X * *</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Prendre en charge ANSI92 SQL. * * *</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Créer des tables.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer une nouvelle base de données.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>ActiveX</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés d'une table existante.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer des relations entre les tables.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>ActiveX</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les paramètres de sécurité.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>ActiveX</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Prise en charge de l'attribut de compression pour les données de colonne.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier des requêtes ou des vues SQL de base stockées.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>ActiveX</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer des requêtes permanentes uniquement accessibles par code</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>ActiveX</p></td>
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
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>Actualiser le cache.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Rendez la base de données réplicable.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Créer des réplicas de base de données.</p></td>
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
<td><p>Modifier les propriétés d'une colonne de tableau.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Uniquement disponible pour la manipulation de bases de données Microsoft Access. Les versions futures de SQL Provider offriront peut-être cette fonctionnalité dans des projets Microsoft Access (.adp).

\*\* Uniquement disponible pour la manipulation de projets Access.

\*\*\*Bien que le moteur de base de données Access prenne en charge certains ANSI 92 SQL, il n'est pas encore entièrement conforme à ANSI92.

1 utilise l'objet **Connection** pour référencer la base de données.

2 utilise l'objet **catalogue** pour référencer la base de données.

3 utilise **** l'objet Replica pour référencer la base de données.

4 utilise l'objet **JetEngine** pour référencer la base de données.


> [!NOTE]
> À la différence des objets DAO, les objets ADO et ADOX peuvent exécuter les actions marquées dans des bases de données autres que Jet tant que le fournisseur de ces bases de données prend en charge cette action.


