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
ms.openlocfilehash: f48b1ab98f6f0f729fdb32b4ff20be09c5d942bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886388"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="aa508-102">TRANSACTION, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="aa508-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="aa508-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa508-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa508-104">Permet de lancer et de conclure des transactions explicites.</span><span class="sxs-lookup"><span data-stu-id="aa508-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa508-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa508-105">Syntax</span></span>

<span data-ttu-id="aa508-106">**Lance une nouvelle transaction**:</span><span class="sxs-lookup"><span data-stu-id="aa508-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="aa508-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="aa508-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="aa508-108">**Conclude une transaction en validant tout le travail effectué au cours de la transaction**:</span><span class="sxs-lookup"><span data-stu-id="aa508-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="aa508-109">VALIDER \[TRANSACTION | TRAVAIL\]</span><span class="sxs-lookup"><span data-stu-id="aa508-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="aa508-110">**Conclude une transaction en annulant tout le travail effectué au cours de la transaction**:</span><span class="sxs-lookup"><span data-stu-id="aa508-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="aa508-111">ROLLBACK \[TRANSACTION | TRAVAIL\]</span><span class="sxs-lookup"><span data-stu-id="aa508-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="aa508-112">Notes</span><span class="sxs-lookup"><span data-stu-id="aa508-112">Remarks</span></span>

<span data-ttu-id="aa508-p101">Les transactions ne démarrant pas automatiquement, vous devez les démarrer de manière explicite à l'aide de l'instruction BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="aa508-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="aa508-p102">Les transactions peuvent être imbriquée sur cinq niveaux. Pour démarrer une transaction imbriquée, utilisez l'instruction BEGIN TRANSACTION dans le contexte d'une transaction existante.</span><span class="sxs-lookup"><span data-stu-id="aa508-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="aa508-117">Les transactions ne sont pas prises en charge pour les tables attachées.</span><span class="sxs-lookup"><span data-stu-id="aa508-117">Transactions are not supported for linked tables.</span></span>

