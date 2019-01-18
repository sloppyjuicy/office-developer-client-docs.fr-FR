---
title: TRANSACTION, instruction (Microsoft Access SQL)
TOCTitle: TRANSACTION statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 828bccfad83320d27f9473d532ab86f73b2fde98
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705518"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION, instruction (Microsoft Access SQL)

**S’applique à**: Access 2013, Office 2013

Permet de lancer et de conclure des transactions explicites.

## <a name="syntax"></a>Syntaxe

**Lance une nouvelle transaction**:

BEGIN TRANSACTION

**Conclude une transaction en validant tout le travail effectué au cours de la transaction**:

VALIDER \[TRANSACTION | TRAVAIL\]

**Conclude une transaction en annulant tout le travail effectué au cours de la transaction**:

ROLLBACK \[TRANSACTION | TRAVAIL\]

## <a name="remarks"></a>Notes

Les transactions ne démarrant pas automatiquement, vous devez les démarrer de manière explicite à l'aide de l'instruction BEGIN TRANSACTION.

Les transactions peuvent être imbriquée sur cinq niveaux. Pour démarrer une transaction imbriquée, utilisez l'instruction BEGIN TRANSACTION dans le contexte d'une transaction existante.

Les transactions ne sont pas prises en charge pour les tables attachées.

