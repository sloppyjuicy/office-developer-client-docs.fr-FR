---
title: Unique Table, Unique Schema, Unique Catalog, propriétés dynamiques (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b2c3c87a820638b74e74c513443261e052e2c4d7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919429"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a>Unique Table, Unique Schema, Unique Catalog, propriétés dynamiques (ADO)


**S’applique à**: Access 2013, Office 2013

Permet de contrôler précisément les modifications apportées à une table de base déterminée dans un objet [Recordset](recordset-object-ado.md) formé par une opération JOIN dans plusieurs tables de base.

  - La propriété **Unique Table** spécifie le nom de la table de base dans laquelle les mises à jour, les insertions et les suppressions sont autorisées.

  - La propriété **Unique Schema** spécifie le *schéma* ou le nom du propriétaire de la table.

  - La propriété **Unique Catalog** spécifie le *catalogue* ou le nom de la base de données contenant la table.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String** qui représente le nom d'une table, d'un schéma ou d'un catalogue.

## <a name="remarks"></a>Notes

La table de base souhaitée est identifiée de manière unique par le nom de son catalogue, de son schéma et de sa table. Lorsque la propriété **Unique Table** est définie, les valeurs des propriétés **Unique Schema** ou **Unique Catalog** sont utilisées pour rechercher la table de base. Il est prévu, mais pas obligatoire, que l'une ou les deux propriétés **Unique Schema** et **Unique Catalog** soient définies avant la propriété **Unique Table**.

La clé primaire de la propriété **Unique Table** est considérée comme la clé primaire de l'ensemble du **Recordset**. Il s'agit de la clé utilisée pour toutes les méthodes nécessitant une clé primaire.

Lorsque la propriété **Unique Table** est définie, la méthode [Delete](delete-method-ado-recordset.md) n'affecte que la table nommée. Les méthodes [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md) et [UpdateBatch](updatebatch-method-ado.md) affectent toutes les tables de base sous-jacentes concernées de l'objet **Recordset**.

La propriété **Unique Table** doit être spécifiée avant d'effectuer des resynchronisations personnalisées. Si la propriété **Unique Table** n'a pas été spécifiée, la propriété [Resync Command](resync-command-property-dynamic-ado.md) n'a aucun effet.

Une erreur d'exécution est générée si aucune table de base unique n'est trouvée.

Ces propriétés dynamiques sont toutes ajoutées à la collection **Properties** de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.

