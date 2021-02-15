---
title: Fonctionnement des commandes non paramétrées
TOCTitle: Operation of non-parameterized commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 720cbaf346b64d4d23b1e3314b06ba941e78b700
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288265"
---
# <a name="operation-of-non-parameterized-commands"></a>Fonctionnement des commandes non paramétrées


**S’applique à** : Access 2013, Office 2013

Pour les commandes non paramétrées, toutes les commandes du fournisseur sont exécutées et les **jeux d'enregistrements** sont créés pendant l'exécution de la commande. Si cette dernière est exécutée de manière synchrone, tous les **jeux d'enregistrements** sont entièrement renseignés. Si une exécution asynchrone a été sélectionnée, le degré de remplissage des **jeux d'enregistrements** dépend du mode de remplissage et de la taille des **jeux d'enregistrements**.

Par exemple, la *commande parent* pourrait renvoyer un **jeu d'enregistrements** des clients d'une société à partir d'une table Customers et la *commande enfant* un **jeu d'enregistrements** des commandes de tous les clients à partir d'une table Orders.

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

For non-parameterized parent-child relationships, each parent and child **Recordset** object must have a column in common to associate them. Les colonnes sont nommées dans la clause RELATE, *colonne parent d’abord,* puis colonne *enfant*. The columns may have different names in their respective **Recordset** objects but must refer to the same information in order to specify a meaningful relation. For example, the **Customers** and **Orders** **Recordset** objects could both have a customerID field. Because the membership of the child **Recordset** is determined by the provider command, it is possible for the child **Recordset** to contain orphaned rows. These orphaned rows are inaccessible without further reshaping.

La mise en forme des données ajoute une colonne de chapitre au **jeu d'enregistrements** parent. Les valeurs de cette colonne sont des références à des lignes du **jeu d'enregistrements** enfant qui répondent à la clause RELATE. Autrement dit, la valeur de la *colonne-parent* d'un ligne parent donnée est identique à celle de la *colonne-enfant* de toutes les lignes de l'enfant de chapitre. Lorsque plusieurs clauses TO sont utilisées dans la même clause RELATE, elle sont implicitement associées via un opérateur AND. Si les colonnes parent de la clause RELATE ne constituent pas une clé pour le **jeu d'enregistrements** parent, une seule ligne enfant peut avoir plusieurs lignes parent.

Lorsque vous accédez à la référence de la colonne de chapitre, ADO extrait automatiquement le **jeu d'enregistrements** représenté par la référence. Notez que dans une commande non paramétrée, bien que tout le **jeu d'enregistrements** enfant ait été extrait, le chapitre ne présente qu'un sous-ensemble de lignes.

Si la colonne ajoutée n’a pas d’*alias-de-chapitre*, un nom lui est automatiquement attribué. Un objet [Field](field-object-ado.md) de la colonne est ajouté à la collection [Fields](fields-collection-ado.md) de l’objet **Recordset** et son type de données est défini sur **adChapter**.

Pour plus d'informations sur la navigation au sein d'un objet **Recordset** hiérarchique, consultez [Accès aux lignes d'un jeu d'enregistrements hiérarchique](accessing-rows-in-a-hierarchical-recordset.md).

