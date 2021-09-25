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
ms.localizationpriority: high
ms.openlocfilehash: e3ed36a0805754f15527b476528d875fa4844dcf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601645"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Utilisé pour amorcer et conclure des transactions explicites.

## <a name="syntax"></a>Syntaxe

**Lance une nouvelle transaction** :

BEGIN TRANSACTION

**Conclut une transaction en validant tout le travail effectué au cours de la transaction** :

COMMIT \[TRANSACTION | WORK\]

**Conclut une transaction en annulant tout le travail effectué au cours de la transaction** :

ROLLBACK \[TRANSACTION | WORK\]

## <a name="remarks"></a>Remarques

Les transactions ne sont pas démarrées automatiquement. Pour démarrer une transaction, vous devez procéder de façon explicite avec la commande BEGIN TRANSACTION.

Des transactions peuvent être imbriquées jusqu’à cinq niveaux. Pour démarrer une transaction imbriquée, utilisez la commande BEGIN TRANSACTION dans le contexte d’une transaction existante.

Les transactions ne sont pas prises en charge pour des tables liées.

