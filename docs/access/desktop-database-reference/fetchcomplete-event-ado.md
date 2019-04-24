---
title: Événement FetchComplete, (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293188"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="526ae-102">Événement FetchComplete, (ADO)</span><span class="sxs-lookup"><span data-stu-id="526ae-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="526ae-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="526ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="526ae-104">L’événement **FetchComplete** est appelé après que tous les enregistrements d’une longue opération asynchrone aient été extraits de l’objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="526ae-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="526ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="526ae-105">Syntax</span></span>

<span data-ttu-id="526ae-106">FetchComplete,*perror*, \*\* adStatus, *Recordset*</span><span class="sxs-lookup"><span data-stu-id="526ae-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="526ae-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="526ae-107">Parameters</span></span>

|<span data-ttu-id="526ae-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="526ae-108">Parameter</span></span>|<span data-ttu-id="526ae-109">Description</span><span class="sxs-lookup"><span data-stu-id="526ae-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="526ae-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="526ae-110">*pError*</span></span> |<span data-ttu-id="526ae-p101">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si **adStatus** a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="526ae-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="526ae-113">*Statu*</span><span class="sxs-lookup"><span data-stu-id="526ae-113">*adStatus*</span></span> |<span data-ttu-id="526ae-114">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="526ae-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="526ae-115">Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="526ae-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="526ae-116">*jeu d'enregistrements*</span><span class="sxs-lookup"><span data-stu-id="526ae-116">*pRecordset*</span></span> |<span data-ttu-id="526ae-p103">Objet **Recordset** représentant le jeu duquel les enregistrements ont été extraits.</span><span class="sxs-lookup"><span data-stu-id="526ae-p103">A **Recordset** object. The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="526ae-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="526ae-119">Remarks</span></span>

<span data-ttu-id="526ae-120">Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchComplete** avec Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="526ae-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

