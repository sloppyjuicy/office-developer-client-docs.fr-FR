---
title: TRANSACTION, instruction (Microsoft Access SQL)
TOCTitle: TRANSACTION Statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 13628ee6d384430691475eb06dbbbdce4e980103
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470878"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="fdd3b-102">TRANSACTION, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="fdd3b-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="fdd3b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fdd3b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fdd3b-104">Permet de lancer et de conclure des transactions explicites.</span><span class="sxs-lookup"><span data-stu-id="fdd3b-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdd3b-105">Syntax</span></span>

<span data-ttu-id="fdd3b-106">Lance une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="fdd3b-106">Initiate a new transaction.</span></span>

<span data-ttu-id="fdd3b-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="fdd3b-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="fdd3b-108">Conclut une transaction en validant tout le travail effectué au cours de la transaction.</span><span class="sxs-lookup"><span data-stu-id="fdd3b-108">Conclude a transaction by committing all work performed during the transaction.</span></span>

<span data-ttu-id="fdd3b-109">VALIDER \[TRANSACTION | TRAVAIL\]</span><span class="sxs-lookup"><span data-stu-id="fdd3b-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="fdd3b-110">Conclut une transaction en annulant tout le travail effectué au cours de la transaction.</span><span class="sxs-lookup"><span data-stu-id="fdd3b-110">Conclude a transaction by rolling back all work performed during the transaction.</span></span>

<span data-ttu-id="fdd3b-111">ROLLBACK \[TRANSACTION | TRAVAIL\]</span><span class="sxs-lookup"><span data-stu-id="fdd3b-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="fdd3b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fdd3b-112">Remarks</span></span>

<span data-ttu-id="fdd3b-p101">Les transactions ne démarrant pas automatiquement, vous devez les démarrer de manière explicite à l'aide de l'instruction BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="fdd3b-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="fdd3b-p102">Les transactions peuvent être imbriquée sur cinq niveaux. Pour démarrer une transaction imbriquée, utilisez l'instruction BEGIN TRANSACTION dans le contexte d'une transaction existante.</span><span class="sxs-lookup"><span data-stu-id="fdd3b-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="fdd3b-117">Les transactions ne sont pas prises en charge pour les tables attachées.</span><span class="sxs-lookup"><span data-stu-id="fdd3b-117">Transactions are not supported for linked tables.</span></span>

