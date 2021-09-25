---
title: TableDef.ConflictTable, propriété (DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 81a28d566abf4225bbb7560cdba11639451f8a16
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589007"
---
# <a name="tabledefconflicttable-property-dao"></a>TableDef.ConflictTable, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie le nom d'une table de conflits contenant les enregistrements de base de données qui sont entrés en conflit lors de la synchronisation de deux réplicas (espaces de travail Microsoft Access uniquement). Valeur de type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* ConflictTable

*expression* Expression qui renvoie un **objet TableDef.**

## <a name="remarks"></a>Remarques

La valeur renvoyée est un type de données **String** qui correspond à une chaîne nulle ("") s'il n'y a pas de table de conflits ou si la base de données n'est pas un réplica.

Si deux utilisateurs sur deux réplicas distincts modifient le même enregistrement de la base de données, les modifications apportées par un utilisateur ne seront pas répercutées sur l'autre réplica. Par conséquent, cet utilisateur doit résoudre les conflits.

Les conflits se produisent au niveau des enregistrements et non entre des champs. Par exemple, si un utilisateur modifie le champ Adresse et qu'un autre utilisateur met à jour le champ Téléphone du même enregistrement, l'une des modifications est refusée. Le refus se produit même s'il est peu probable que la modification acceptée et la modification refusée entraînent un conflit réel.

Le mécanisme de synchronisation gère les conflits d'enregistrements en créant des tables de conflits, qui contiennent les informations qui auraient été insérées dans la table si la modification avait réussi. Vous pouvez consulter ces tables de conflits et les parcourir ligne par ligne pour résoudre les conflits.

Toutes les tables de conflit sont nommées conflit de table, où table est le nom d’origine de la table, tronquée à la longueur de nom de \_ table maximale.

