---
title: Recordset2.BatchCollisions, propriété (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 1e8f494d74413470d819b5a0cd42449f26f2d8f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606015"
---
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2.BatchCollisions, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* BatchCollisions

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Cette propriété contient un tableau de signets vers des lignes qui ont présenté un conflit au cours du dernier appel de la méthode **[Update](recordset2-update-method-dao.md)** par lot. La propriété **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** indique le nombre d'éléments présents dans le tableau.

Si vous affectez à la propriété [**Bookmark**](recordset2-bookmark-property-dao.md) de l'objet **Recordset** de travail des valeurs de signet du tableau **BatchCollisions**, vous pouvez accéder à chaque enregistrement qui n'a pas pu achever la dernière opération de mise à jour par lot

Après correction des enregistrements présentant des conflits, il est possible d'appeler à nouveau une méthode **Update** par lot. À ce stade, DAO tente d'exécuter une autre mise à jour par lot et la propriété **BatchCollisions** reflète à nouveau le jeu d'enregistrements ayant échoué à la deuxième tentative. Tous les enregistrements dont la mise à jour a réussi lors de la tentative précédente ne sont pas repris dans la tentative actuelle car leur propriété **[RecordStatus](recordset2-recordstatus-property-dao.md)** a désormais la valeur dbRecordUnmodified. Ce processus peut se poursuivre aussi longtemps que des conflits surviennent ou jusqu'à ce que vous abandonniez les mises à jour et fermiez le jeu de résultats.

Ce tableau est recréé chaque fois que vous exécutez une méthode **Update** par lot.

