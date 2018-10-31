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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="71b5e-102">TRANSACTION, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="71b5e-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="71b5e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="71b5e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="71b5e-104">Permet de lancer et de conclure des transactions explicites.</span><span class="sxs-lookup"><span data-stu-id="71b5e-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b5e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71b5e-105">Syntax</span></span>

<span data-ttu-id="71b5e-106">**Lance une nouvelle transaction**:</span><span class="sxs-lookup"><span data-stu-id="71b5e-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="71b5e-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="71b5e-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="71b5e-108">**Conclude une transaction en validant tout le travail effectué au cours de la transaction**:</span><span class="sxs-lookup"><span data-stu-id="71b5e-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="71b5e-109">VALIDER \[TRANSACTION | TRAVAIL\]</span><span class="sxs-lookup"><span data-stu-id="71b5e-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="71b5e-110">**Conclude une transaction en annulant tout le travail effectué au cours de la transaction**:</span><span class="sxs-lookup"><span data-stu-id="71b5e-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="71b5e-111">ROLLBACK \[TRANSACTION | TRAVAIL\]</span><span class="sxs-lookup"><span data-stu-id="71b5e-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="71b5e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="71b5e-112">Remarks</span></span>

<span data-ttu-id="71b5e-p101">Les transactions ne démarrant pas automatiquement, vous devez les démarrer de manière explicite à l'aide de l'instruction BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="71b5e-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="71b5e-p102">Les transactions peuvent être imbriquée sur cinq niveaux. Pour démarrer une transaction imbriquée, utilisez l'instruction BEGIN TRANSACTION dans le contexte d'une transaction existante.</span><span class="sxs-lookup"><span data-stu-id="71b5e-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="71b5e-117">Les transactions ne sont pas prises en charge pour les tables attachées.</span><span class="sxs-lookup"><span data-stu-id="71b5e-117">Transactions are not supported for linked tables.</span></span>

