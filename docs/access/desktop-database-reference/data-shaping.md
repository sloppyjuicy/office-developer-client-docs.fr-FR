---
title: Mise en forme des données (référence de base de données de bureau Access)
TOCTitle: Data shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ad507ac8c963f1d6ead7bc3bf444e694d83f90e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295036"
---
# <a name="data-shaping"></a>Mise en forme des données

**S’applique à** : Access 2013, Office 2013

La mise en forme des données permet de définir les colonnes d'un objet **Recordset** mis en forme, les relations entre les entités représentées par les colonnes et le mode de remplissage de l'objet **Recordset** avec des données.

Les colonnes d'un objet **Recordset** mis en forme peuvent contenir des données provenant d'un fournisseur de données tel que Microsoft SQL Server, des références à un autre objet **Recordset**, des valeurs calculées d'après une seule ligne d'un objet **Recordset**, des valeurs dérivées d'une opération portant sur une colonne entière d'un objet **Recordset**, ou ces colonnes peuvent encore être des colonnes vides, récemment créées.

When you retrieve the value of a column that contains a reference to another **Recordset**, ADO automatically returns the actual **Recordset** represented by the reference. A **Recordset** that contains another **Recordset** is called a hierarchical recordset. Les jeux d'enregistrements hiérarchiques présentent une relation *parent-enfant* , dans laquelle le *parent* est le jeu d'enregistrements contenant et l' *enfant* est l'objet Recordset contenu. La référence à un **objet Recordset** est en fait une référence à un sous-ensemble de l'enfant, appelé un *chapitre*. A single parent may reference more than one child **Recordset**.

La syntaxe de commandes de mise en forme permet de créer par programme un objet **Recordset** mis en forme. Vous pouvez ensuite accéder aux composants de l'objet **Recordset** par programme ou via un contrôle visuel approprié. Une commande de mise en forme est émise comme tout autre texte de commande ADO.

Vous pouvez créer des objets **Recordset** hiérarchiques de deux manières différentes grâce à la syntaxe de commandes de mise en forme. La première consiste à ajouter un objet **Recordset** enfant à l'objet **Recordset** parent. Généralement, le parent et l'enfant possèdent en commun au moins un colonne : la valeur de la colonne dans une ligne du parent est identique à celle de la colonne dans toutes les lignes au niveau de l'enfant.

The second way generates a parent **Recordset** from a child **Recordset**. The records in the child **Recordset** are grouped, typically using the BY clause, and one row is added to the parent **Recordset** for each resulting group in the child. If the BY clause is omitted, the child **Recordset** will form a single group and the parent **Recordset** will contain exactly one row. This is useful for computing "grand total" aggregates over the entire child **Recordset**.

Regardless of which way the parent **Recordset** is formed, it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also have columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may have columns which contain an expression on the row in the **Recordset**, as well as columns which are new and initially empty.

Vous pouvez imbriquer des objets **Recordset** hiérarchiques à n'importe quelle profondeur (en d'autres termes, créer des objets **Recordset** enfants d'autres objets **Recordset** enfants, etc.).

Vous pouvez accéder aux composants **Recordset** de l'objet **Recordset** mis en forme par programme ou via un contrôle visuel adéquat.

Pour obtenir des exemples de commandes de mise en forme et des hiérarchies qui en résultent, voir « Utilisation de Microsoft Data Shaping Service pour OLE DB ».

Cette section contient les rubriques suivantes :

- [Remise en forme des données](reshaping.md)
- [Agrégats petit-enfant](grandchild-aggregates.md)
- [Commandes paramétrées avec l’intervention de commandes COMPUTE](parameterized-commands-with-intervening-compute-commands.md)
- [Persistance de recordsets hiérarchiques](persisting-hierarchical-recordsets.md)
