---
title: Data Shaping (référence de base de données du bureau Access)
TOCTitle: Data Shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 686c860ef9d8975b02391fedcea8f4b6f4e0b9bb
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862295"
---
# <a name="data-shaping"></a>Mise en forme des données


**S’applique à**: Access 2013 | Office 2013

La mise en forme des données permet de définir les colonnes d'un objet **Recordset** mis en forme, les relations entre les entités représentées par les colonnes et le mode de remplissage de l'objet **Recordset** avec des données.

Les colonnes d'un objet **Recordset** mis en forme peuvent contenir des données provenant d'un fournisseur de données tel que Microsoft SQL Server, des références à un autre objet **Recordset**, des valeurs calculées d'après une seule ligne d'un objet **Recordset**, des valeurs dérivées d'une opération portant sur une colonne entière d'un objet **Recordset**, ou ces colonnes peuvent encore être des colonnes vides, récemment créées.

Lorsque vous récupérez la valeur d’une colonne qui contient une référence à un autre **objet Recordset**, ADO retourne automatiquement le réel **Recordset** représenté par la référence. Un **jeu d’enregistrements** contenant un autre **jeu d’enregistrements** est appelé un jeu d’enregistrements hiérarchique. Jeux d’enregistrements hiérarchiques présente une relation *parent-enfant* dans laquelle le *parent* est l’objet recordset contenant et l' *enfant* est le jeu contenu. La référence à un **objet Recordset** est en fait une référence à un sous-ensemble de l’enfant, appelé un *chapitre*. **Plus d’un objet Recordset**peut faire référence à un seul parent.

La syntaxe de commandes de mise en forme permet de créer par programme un objet **Recordset** mis en forme. Vous pouvez ensuite accéder aux composants de l'objet **Recordset** par programme ou via un contrôle visuel approprié. Une commande de mise en forme est émise comme tout autre texte de commande ADO.

Vous pouvez créer des objets **Recordset** hiérarchiques de deux manières différentes grâce à la syntaxe de commandes de mise en forme. La première consiste à ajouter un objet **Recordset** enfant à l'objet **Recordset** parent. Généralement, le parent et l'enfant possèdent en commun au moins un colonne : la valeur de la colonne dans une ligne du parent est identique à celle de la colonne dans toutes les lignes au niveau de l'enfant.

La deuxième méthode génère un **jeu d’enregistrements** parent à partir d’un **objet Recordset**enfant. Les enregistrements dans **l’objet Recordset** enfant sont regroupés, généralement à l’aide de la clause BY et une ligne est ajoutée à **l’objet Recordset** parent pour chaque groupe résultant dans l’enfant. Si la clause BY est omise, **l’objet Recordset** enfant forment un seul groupe et **l’objet Recordset** parent contient exactement une ligne. Cela est utile pour calculer des agrégats de « totaux » sur l’intégralité de **l’objet Recordset**enfant.

Quelle que soit la façon dont le parent de **que jeu d’enregistrements** est créé, il contient une colonne de chapitre qui sert à associer à un **objet Recordset**enfant. Si vous le souhaitez, **l’objet Recordset** parent peut également posséder des colonnes qui contiennent des fonctions d’agrégation (somme, MIN, MAX et ainsi de suite) sur les lignes enfants. Le parent et **l’objet Recordset** enfant peut-être colonnes contenant une expression sur la ligne dans le **jeu d’enregistrements**, ainsi que les colonnes qui sont nouvelles et initialement vides.

Vous pouvez imbriquer des objets **Recordset** hiérarchiques à n'importe quelle profondeur (en d'autres termes, créer des objets **Recordset** enfants d'autres objets **Recordset** enfants, etc.).

Vous pouvez accéder aux composants **Recordset** de l'objet **Recordset** mis en forme par programme ou via un contrôle visuel adéquat.

Pour obtenir des exemples de commandes de mise en forme et des hiérarchies qui en résultent, voir « Utilisation de Microsoft Data Shaping Service pour OLE DB ».

Cette section comprend les rubriques suivantes :

- [Remise en forme des données](reshaping.md)

- [Agrégats petits-enfants](grandchild-aggregates.md)

- [Commandes paramétrées avec des commandes COMPUTE intermédiaires](parameterized-commands-with-intervening-compute-commands.md)

- [Persistance des objets Recordset hiérarchiques](persisting-hierarchical-recordsets.md)