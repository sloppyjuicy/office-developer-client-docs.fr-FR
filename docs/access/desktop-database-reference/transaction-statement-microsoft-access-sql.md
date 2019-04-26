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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314146"
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

