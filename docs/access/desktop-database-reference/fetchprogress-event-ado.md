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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703516"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="805dc-102">FetchProgress, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="805dc-102">FetchProgress event (ADO)</span></span>

<span data-ttu-id="805dc-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="805dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="805dc-104">L'événement **FetchProgress** est régulièrement appelé pendant une opération asynchrone de longue durée, afin de signaler le nombre de lignes déjà extraites de l'objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="805dc-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="805dc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="805dc-105">Syntax</span></span>

<span data-ttu-id="805dc-106">FetchProgress*progression*, *MaxProgress*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="805dc-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="805dc-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="805dc-107">Parameters</span></span>

|<span data-ttu-id="805dc-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="805dc-108">Parameter</span></span>|<span data-ttu-id="805dc-109">Description</span><span class="sxs-lookup"><span data-stu-id="805dc-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="805dc-110">*Progress*</span><span class="sxs-lookup"><span data-stu-id="805dc-110">*Progress*</span></span> |<span data-ttu-id="805dc-111">Valeur de type **Long** indiquant le nombre d'enregistrements déjà extraits par l'opération d'extraction.</span><span class="sxs-lookup"><span data-stu-id="805dc-111">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>|
|<span data-ttu-id="805dc-112">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="805dc-112">*MaxProgress*</span></span> |<span data-ttu-id="805dc-113">Valeur de type **Long** indiquant le nombre maximal prévu d'enregistrements à récupérer.</span><span class="sxs-lookup"><span data-stu-id="805dc-113">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>|
|<span data-ttu-id="805dc-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="805dc-114">*adStatus*</span></span> |<span data-ttu-id="805dc-115">Valeur d'état [EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="805dc-115">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>|
|<span data-ttu-id="805dc-116">*Connection*</span><span class="sxs-lookup"><span data-stu-id="805dc-116">*pRecordset*</span></span> |<span data-ttu-id="805dc-117">Objet **Recordset** représentant le jeu duquel les enregistrements sont extraits.</span><span class="sxs-lookup"><span data-stu-id="805dc-117">A **Recordset** object that is the object for which the records are being retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="805dc-118">Notes</span><span class="sxs-lookup"><span data-stu-id="805dc-118">Remarks</span></span>

<span data-ttu-id="805dc-119">Lorsque vous utilisez **FetchProgress** avec un **objet Recordset**enfant, n’oubliez pas que les valeurs des paramètres *Progress* et *MaxProgress* sont dérivées de l’ensemble de lignes [Service de curseur](microsoft-cursor-service-for-ole-db-ado-service-component.md) sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="805dc-119">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="805dc-120">Les valeurs retournées représentent le nombre total d'enregistrements de l'ensemble de lignes sous-jacent et pas seulement ceux du chapitre actif.</span><span class="sxs-lookup"><span data-stu-id="805dc-120">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="805dc-121">[!REMARQUE] Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchProgress** avec Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="805dc-121">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


