---
title: FetchComplete, événement (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701962"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="4e0a2-102">FetchComplete, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="4e0a2-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="4e0a2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e0a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e0a2-104">L'événement **FetchComplete** est appelé après que tous les enregistrements d'une longue opération asynchrone aient été extraits de l'objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4e0a2-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0a2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e0a2-105">Syntax</span></span>

<span data-ttu-id="4e0a2-106">FetchComplete*pError*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="4e0a2-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="4e0a2-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4e0a2-107">Parameters</span></span>

|<span data-ttu-id="4e0a2-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="4e0a2-108">Parameter</span></span>|<span data-ttu-id="4e0a2-109">Description</span><span class="sxs-lookup"><span data-stu-id="4e0a2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4e0a2-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="4e0a2-110">*pError*</span></span> |<span data-ttu-id="4e0a2-p101">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si **adStatus** a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="4e0a2-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="4e0a2-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="4e0a2-113">*adStatus*</span></span> |<span data-ttu-id="4e0a2-114">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="4e0a2-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="4e0a2-115">Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4e0a2-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="4e0a2-116">*Connection*</span><span class="sxs-lookup"><span data-stu-id="4e0a2-116">*pRecordset*</span></span> |<span data-ttu-id="4e0a2-p103">Objet **Recordset** représentant le jeu duquel les enregistrements ont été extraits.</span><span class="sxs-lookup"><span data-stu-id="4e0a2-p103">A **Recordset** object. The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4e0a2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4e0a2-119">Remarks</span></span>

<span data-ttu-id="4e0a2-120">Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchComplete** avec Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4e0a2-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

