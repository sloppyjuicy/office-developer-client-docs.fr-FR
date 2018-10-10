---
title: Cancel, méthode (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcd37f8736b7ab4b953480cd28daeb3080abe07f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469895"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="65cf1-102">Cancel, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="65cf1-102">Cancel Method (RDS)</span></span>


<span data-ttu-id="65cf1-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="65cf1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="65cf1-104">Annule l'exécution d'un appel de méthode asynchrone en attente.</span><span class="sxs-lookup"><span data-stu-id="65cf1-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="65cf1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65cf1-105">Syntax</span></span>

<span data-ttu-id="65cf1-106">*RDS*.</span><span class="sxs-lookup"><span data-stu-id="65cf1-106">*RDS*.</span></span> <span data-ttu-id="65cf1-107">*DataControl*. Annuler</span><span class="sxs-lookup"><span data-stu-id="65cf1-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="65cf1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="65cf1-108">Remarks</span></span>

<span data-ttu-id="65cf1-109">Lorsque vous appelez **Cancel**, [ReadyState](readystate-property-rds.md) prend automatiquement la valeur **adcReadyStateLoaded** et l'objet [Recordset](recordset-object-ado.md) sera vide.</span><span class="sxs-lookup"><span data-stu-id="65cf1-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

