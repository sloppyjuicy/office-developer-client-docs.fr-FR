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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="8a18c-102">TRANSACTION, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8a18c-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="8a18c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a18c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a18c-104">Utilisé pour amorcer et conclure des transactions explicites.</span><span class="sxs-lookup"><span data-stu-id="8a18c-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a18c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a18c-105">Syntax</span></span>

<span data-ttu-id="8a18c-106">**Lance une nouvelle transaction** :</span><span class="sxs-lookup"><span data-stu-id="8a18c-106">Initiate a new transaction.</span></span>

<span data-ttu-id="8a18c-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="8a18c-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="8a18c-108">**Conclut une transaction en validant tout le travail effectué au cours de la transaction** :</span><span class="sxs-lookup"><span data-stu-id="8a18c-108">Conclude a transaction by committing all work performed during the transaction.</span></span>

<span data-ttu-id="8a18c-109">COMMIT \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="8a18c-109">COMMIT [TRANSACTION | WORK]</span></span>

<span data-ttu-id="8a18c-110">**Conclut une transaction en annulant tout le travail effectué au cours de la transaction** :</span><span class="sxs-lookup"><span data-stu-id="8a18c-110">Conclude a transaction by rolling back all work performed during the transaction.</span></span>

<span data-ttu-id="8a18c-111">ROLLBACK \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="8a18c-111">ROLLBACK [TRANSACTION | WORK]</span></span>

## <a name="remarks"></a><span data-ttu-id="8a18c-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a18c-112">Remarks</span></span>

<span data-ttu-id="8a18c-p101">Les transactions ne sont pas démarrées automatiquement. Pour démarrer une transaction, vous devez procéder de façon explicite avec la commande BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="8a18c-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="8a18c-p102">Des transactions peuvent être imbriquées jusqu’à cinq niveaux. Pour démarrer une transaction imbriquée, utilisez la commande BEGIN TRANSACTION dans le contexte d’une transaction existante.</span><span class="sxs-lookup"><span data-stu-id="8a18c-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="8a18c-117">Les transactions ne sont pas prises en charge pour des tables liées.</span><span class="sxs-lookup"><span data-stu-id="8a18c-117">Transactions are not supported for linked tables.</span></span>

