---
title: Utilisation des objets de données ActiveX
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470213"
---
# <a name="using-activex-data-objects"></a>Utilisation des objets de données ActiveX


**S’applique à**: Access 2013 | Office 2013

Microsoft Access propose trois modèles d'objet à utiliser pour la création, la maintenance et la gestion de vos bases de données Access et de leurs données liées à l'aide de Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Objets de données Microsoft ActiveX (ADO)

ADO contient les objets nécessaires pour créer, maintenir et supprimer des enregistrements dans une source de données.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. for DDL and Security (ADOX)

ADOX comprend les objets DDL (Data Definition Language, langage de définition de données) nécessaires pour créer une nouvelle base de données et ses objets contenus en plus des objets nécessaires pour gérer la sécurité.

**Microsoft Jet and Replication Objects 2.5 Library (JRO)**

Du fait que les objets ADO ont été créés pour fonctionner avec de nombreuses bases de données, en plus des bases de données Microsoft Jet, la fonctionnalité propre à Jet a été intégrée dans la bibliothèque JRO.

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
<th><p>Fonctionnalités</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(Uniquement MDB)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Créer des jeux d’enregistrements</p></td>
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier des propriétés de démarrage</p></td>
<td><p>X </p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Prendre en charge ANSI92 SQL***</p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Créer des tables</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer une nouvelle base de données</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier des propriétés de table existantes</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer des relations de table</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier des paramètres de sécurité</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Prendre en charge l’attribut de compression pour les données de colonne</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier des requêtes ou des vues SQL de base stockées</p></td>
<td><p>X </p></td>
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
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Compacter/coder une base de données</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Actualiser mémoire cache</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
</tr>
<tr class="odd">
<td><p>Rendre une base de données réplicable</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Faire des réplicas de base de données</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Synchroniser des réplicas</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Modifier des propriétés de base de données</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer des propriétés de base de données personnalisées</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés d’une colonne de table</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Uniquement disponible pour la manipulation de bases de données Microsoft Access. Les versions futures de SQL Provider offriront peut-être cette fonctionnalité dans des projets Microsoft Access (.adp).

\*\* Uniquement disponible pour la manipulation de projets Access.

\*\*\* Même si le moteur de base de données Access prend en charge certains codes ANSI 92 SQL, il n'est pas encore totalement compatible à ANSI92.

1Utilise un objet **Connection** pour faire référence à une base de données

2Utilise un objet **Catalog** pour faire référence à une base de données

3Utilise un objet **Replica** pour faire référence à une base de données

4Utilise un objet **JetEngine** pour faire référence à une base de données


> [!NOTE]
> <P>[!REMARQUE] À la différence des objets DAO, les objets ADO et ADOX peuvent exécuter les actions indiquées dans des bases de données autres que Jet tant que le fournisseur de celles-ci prend en charge ces actions.</P>


