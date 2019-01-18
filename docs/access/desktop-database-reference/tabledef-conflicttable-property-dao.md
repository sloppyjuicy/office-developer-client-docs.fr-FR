---
title: Propriété TableDef.ConflictTable (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 0189a5163dd5e225ad34841264cf84e85785d7fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718916"
---
# <a name="tabledefconflicttable-property-dao"></a>Propriété TableDef.ConflictTable (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie le nom d'une table de conflits contenant les enregistrements de base de données qui sont entrés en conflit lors de la synchronisation de deux réplicas (espaces de travail Microsoft Access uniquement). Valeur de type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . ConflictTable

*expression* Expression qui renvoie un objet **TableDef** .

## <a name="remarks"></a>Remarques

La valeur renvoyée est un type de données **String** qui correspond à une chaîne nulle ("") s'il n'y a pas de table de conflits ou si la base de données n'est pas un réplica.

Si deux utilisateurs sur deux réplicas distincts modifient le même enregistrement de la base de données, les modifications apportées par un utilisateur ne seront pas répercutées sur l'autre réplica. Par conséquent, cet utilisateur doit résoudre les conflits.

Les conflits se produisent au niveau des enregistrements et non entre des champs. Par exemple, si un utilisateur modifie le champ Adresse et qu'un autre utilisateur met à jour le champ Téléphone du même enregistrement, l'une des modifications est refusée. Le refus se produit même s'il est peu probable que la modification acceptée et la modification refusée entraînent un conflit réel.

Le mécanisme de synchronisation gère les conflits d'enregistrements en créant des tables de conflits, qui contiennent les informations qui auraient été insérées dans la table si la modification avait réussi. Vous pouvez consulter ces tables de conflits et les parcourir ligne par ligne pour résoudre les conflits.

Toutes les tables de conflits sont nommés table\_conflit, où table est le nom d’origine de la table, restreint à la longueur du nom de table maximale.

