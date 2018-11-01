---
title: Utiliser des objets de données ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access propose trois modèles d’objet à utiliser pour la création, de maintenance et la gestion de vos bases de données Access et leurs données liées à l’aide de Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7e8e7e6abeea9cca86c928760eddb990517a207
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887508"
---
# <a name="use-activex-data-objects"></a>Utiliser des objets de données ActiveX

**S’applique à**: Access 2013, Office 2013

Microsoft Access propose trois modèles d’objet à utiliser pour la création, de maintenance et la gestion de vos bases de données Access et leurs données liées à l’aide de Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Objets de données Microsoft ActiveX (ADO)

ADO contient les objets nécessaires pour créer, maintenir et supprimer des enregistrements dans une source de données.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. pour DDL and security (ADOX)

ADOX comprend les objets de langage de définition de données (DDL) nécessaires pour créer une nouvelle base de données et ses objets contenus en plus des objets nécessaires pour gérer la sécurité.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Modèle Microsoft Jet and Replication Objects 2.5 library (JRO)

Étant donné que les objets ADO ont été conçus pour fonctionner avec nombreuses bases de données en plus des bases de données Microsoft Jet, la fonctionnalité propre à Jet a été intégrée dans la bibliothèque JRO.

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
(MDB uniquement)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Créer des jeux d’enregistrements.</p></td>
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés de démarrage.</p></td>
<td><p>X </p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Prendre en charge ANSI92 SQL.* **</p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Créer des tableaux.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer la nouvelle base de données.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés de table existantes.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer des relations entre les tables.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les paramètres de sécurité.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Prise en charge pour l’attribut de Compression pour les données de colonne.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les requêtes SQL ou des vues stockées base.</p></td>
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
<td><p>Compacter/coder une base de données.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Actualiser le cache.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
</tr>
<tr class="odd">
<td><p>Rendre la base de données réplicable.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Vérifiez les réplicas de base de données.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Synchroniser des réplicas.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés de base de données.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Créer des propriétés de base de données personnalisée.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modifier les propriétés de colonne de table.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Uniquement disponible pour la manipulation de bases de données Microsoft Access. Les versions futures de SQL Provider offriront peut-être cette fonctionnalité dans des projets Microsoft Access (.adp).

\*\* Uniquement disponible pour la manipulation de projets Access.

\*\*\*Bien que le moteur de base de données Access ne prend pas en charge certains codes ANSI 92 SQL, il n’est pas encore totalement compatible à ANSI92.

1 objet utilise **connexion** à la base de données de référence.

Objet utilise **catalogue** 2 à la base de données de référence.

Objet 3 utilise **réplica** de base de données de référence.

4 utilise **JetEngine** un objet à la base de données de référence.


> [!NOTE]
> DAO, les objets ADO et ADOX peuvent exécuter les actions indiquées dans les bases de données autres que Jet tant que le fournisseur de celles-ci prend en charge cette action.


