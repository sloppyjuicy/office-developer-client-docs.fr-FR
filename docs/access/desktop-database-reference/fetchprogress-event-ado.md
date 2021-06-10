---
title: FetchProgress, événement (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293181"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="d53f3-102">FetchProgress, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="d53f3-102">FetchProgress event (ADO)</span></span>

<span data-ttu-id="d53f3-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d53f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d53f3-104">L’événement **FetchProgress** est régulièrement appelé pendant une opération asynchrone de longue durée, afin de signaler le nombre de lignes déjà extraites de l’objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d53f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d53f3-105">Syntax</span></span>

<span data-ttu-id="d53f3-106">FetchProgress *Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="d53f3-106">FetchProgress *Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="d53f3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d53f3-107">Parameters</span></span>

|<span data-ttu-id="d53f3-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d53f3-108">Parameter</span></span>|<span data-ttu-id="d53f3-109">Description</span><span class="sxs-lookup"><span data-stu-id="d53f3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d53f3-110">*Progress*</span><span class="sxs-lookup"><span data-stu-id="d53f3-110">*Progress*</span></span> |<span data-ttu-id="d53f3-111">Valeur de type **Long** indiquant le nombre d'enregistrements déjà extraits par l'opération d'extraction.</span><span class="sxs-lookup"><span data-stu-id="d53f3-111">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>|
|<span data-ttu-id="d53f3-112">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="d53f3-112">*MaxProgress*</span></span> |<span data-ttu-id="d53f3-113">Valeur de type **Long** indiquant le nombre maximal prévu d'enregistrements à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d53f3-113">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>|
|<span data-ttu-id="d53f3-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="d53f3-114">*adStatus*</span></span> |<span data-ttu-id="d53f3-115">Valeur d'état [EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="d53f3-115">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>|
|<span data-ttu-id="d53f3-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="d53f3-116">*pRecordset*</span></span> |<span data-ttu-id="d53f3-117">Objet **Recordset** représentant le jeu duquel les enregistrements sont extraits.</span><span class="sxs-lookup"><span data-stu-id="d53f3-117">A **Recordset** object that is the object for which the records are being retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d53f3-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="d53f3-118">Remarks</span></span>

<span data-ttu-id="d53f3-p101">En cas d’utilisation de **FetchProgress** avec un objet **Recordset** enfant, il est important de savoir que les valeurs des paramètres *Progress* et *MaxProgress* sont dérivées de l’ensemble de lignes du [service de curseur](microsoft-cursor-service-for-ole-db-ado-service-component.md). Les valeurs retournées représentent le nombre total d’enregistrements de l’ensemble de lignes sous-jacent et pas seulement ceux du chapitre actif.</span><span class="sxs-lookup"><span data-stu-id="d53f3-p101">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset. The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="d53f3-121">[!REMARQUE] Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchProgress** avec Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d53f3-121">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


