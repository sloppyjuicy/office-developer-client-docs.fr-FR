---
title: Recordset.BatchCollisions Property (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4818ff1ceda746a0acb72a47e87eda58f87b2dfc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882601"
---
# <a name="recordsetbatchcollisions-property-dao"></a>Recordset.BatchCollisions Property (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . BatchCollisions

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Cette propriété contient un tableau de signets permettant d'accéder aux lignes qui ont subi des collisions lors de la dernière opération **[Update](recordset-update-method-dao.md)** par lot. La propriété **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** indique le nombre d'éléments contenus dans le tableau.

Si vous définissez la propriété **[Bookmark](recordset-object-dao.md)** de l'objet **[Recordset](recordset-bookmark-property-dao.md)** de travail sur des signets du tableau **BatchCollisions**, vous pouvez accéder à chaque enregistrement dont la dernière opération Update par lot a échoué.

Une fois les enregistrements en collision corrigés, il est possible de rappeler la méthode **Update** en mode par lot. À ce stade, DAO tente d'exécuter une autre mise à jour par lot et la propriété **BatchCollisions** indique à nouveau le jeu d'enregistrements dont la seconde tentative a échoué. Les enregistrements dont la tentative précédente a réussi ne sont pas envoyés dans la tentative en cours, car ils possèdent à présent la propriété **[RecordStatus](recordset-recordstatus-property-dao.md)** dbRecordUnmodified. Ce processus peut se poursuivre jusqu'à ce que toutes les collisions soient résolues ou que vous abandonniez les mises à jour et fermiez le jeu de résultats.

Ce tableau est recréé à chaque exécution d'une méthode **Update** par lot.

