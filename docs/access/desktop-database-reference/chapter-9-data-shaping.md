---
title: 'Chapitre 9 : Mise en forme de données'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ad9d5e989bc1c6f4a54fb4882cfe3c3e357fd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296422"
---
# <a name="chapter-9-data-shaping"></a>Chapitre 9 : Mise en forme de données

**S’applique à** : Access 2013, Office 2013

La *mise en forme des données* permet d’interroger une source de données et de retourner un objet [Recordset](recordset-object-ado.md) qui représente une relation parent-enfant entre deux ou plusieurs entités logiques (une hiérarchie). 

Des clients et des commandes constituent un exemple de relation hiérarchique classique. Ainsi, à chaque client d'une base de données correspond zéro ou plusieurs commandes. Bien que les requêtes SQL normales fournissent un moyen d'extraire les données à l'aide de la syntaxe JOIN, celles-ci peuvent s'avérer inefficaces et difficiles à manipuler, car des données parentes redondantes sont répétées dans chaque enregistrement renvoyé pour une relation parent-enfant donnée. La mise en forme des données peut associer un seul enregistrement parent de l'objet **Recordset** parent à plusieurs enregistrements enfants de l'objet **Recordset** enfant, ce qui évite la redondance inhérente à une opération de jointure. Nombreux sont ceux qui trouvent le modèle de programmation de plusieurs objets **Recordset** parent-enfants plus naturel et plus facile à manipuler que le modèle JOIN reposant sur un seul objet **Recordset**.

La syntaxe de mise en forme des données fournit aussi d'autres fonctionnalités. Elle permet notamment aux développeurs de créer de nouveaux objets **Recordset** sans source de données sous-jacente à l'aide du mot-clé NEW. Ce mot-clé permet de décrire les champs des objets **Recordset** parents et enfants. Le nouvel objet **Recordset** peut être rempli avec des données et stocké de façon persistante. La syntaxe de mise en forme permet également aux développeurs d'effectuer divers calculs ou agrégations (par exemple, SUM, AVG et MAX) sur les champs enfants ainsi que de créer un objet **Recordset** parent à partir d'un objet **Recordset** enfant en groupant les enregistrements dans l'enregistrement enfant et en plaçant une ligne dans l'enregistrement parent pour chaque groupe dans l'enfant.

Consultez les rubriques suivantes pour en savoir plus sur la mise en forme des données :

- [Fournisseurs requis pour la mise en forme des données](required-providers-for-data-shaping.md)
- [Shape Compute, clause](shape-compute-clause.md)
- [Fabrication de recordsets hiérarchiques](fabricating-hierarchical-recordsets.md)
- [Accès à des lignes dans un recordset hiérarchique](accessing-rows-in-a-hierarchical-recordset.md)
- [Grammaire de forme formelle](formal-shape-grammar.md)
- [Visual Basic for Applications functions](visual-basic-for-applications-functions.md)
- [Shape Append, clause (ADO)](shape-append-clause.md)
- [Mise en forme des données (ADO)](data-shaping.md)
- [Commandes shape en général (ADO)](shape-commands-in-general.md)

