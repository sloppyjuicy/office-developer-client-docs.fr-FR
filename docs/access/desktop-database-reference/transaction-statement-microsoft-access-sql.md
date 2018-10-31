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
ms.openlocfilehash: 6d93fc90beded30d96b4db54c35ab3046da06899
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862662"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION, instruction (Microsoft Access SQL)

**S’applique à**: Access 2013 | Office 2013

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

