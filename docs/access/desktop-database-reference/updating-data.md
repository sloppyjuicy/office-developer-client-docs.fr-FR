---
title: Mise à jour des données (référence de base de données de bureau Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313565"
---
# <a name="updating-data"></a>Mise à jour des données


**S’applique à** : Access 2013, Office 2013

Le comportement et les fonctionnalités de mise à jour dépendent, pour une large part, du mode de mise à jour (type de verrou), du type de curseur, et de l'emplacement du curseur.

Utilisez la méthode **Update** pour enregistrer toutes les modifications apportées à l'enregistrement actif d'un objet **Recordset** depuis l'appel de la méthode **AddNew** ou depuis la modification des valeurs des champs d'un enregistrement existant. L'objet **Recordset** doit prendre en charge les mises à jour.

Si l'objet **Recordset** prend en charge les mises à jour par lot, il est possible d'enregistrer dans un cache local les modifications apportées à un ou plusieurs enregistrements jusqu'à ce que vous appeliez la méthode **UpdateBatch**. Si vous êtes en train de modifier l'enregistrement actif ou d'ajouter un nouvel enregistrement lorsque vous appelez la méthode **UpdateBatch**, ADO appelle automatiquement la méthode **Update** pour enregistrer toutes les modifications en cours de l'enregistrement actif avant de transmettre les modifications par lot au fournisseur.

L'enregistrement actif reste actif après l'appel des méthodes **Update** ou **UpdateBatch**.

Cette section contient les rubriques suivantes :

- [Mode immédiat](immediate-mode.md)
- [Traitement de transactions](transaction-processing.md)
- [Batch mode (ADO)](batch-mode.md)

