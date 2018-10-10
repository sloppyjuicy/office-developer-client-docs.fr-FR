---
title: FetchComplete, événement (ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 299fec4a831bbde5d3fd2d58e0f76edb2acea0f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471159"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="99fc7-102">FetchComplete, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="99fc7-102">FetchComplete Event (ADO)</span></span>


<span data-ttu-id="99fc7-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="99fc7-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="99fc7-104">L'événement **FetchComplete** est appelé après que tous les enregistrements d'une longue opération asynchrone aient été extraits de l'objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="99fc7-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="99fc7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99fc7-105">Syntax</span></span>

<span data-ttu-id="99fc7-106">FetchComplete*pError*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="99fc7-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="99fc7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99fc7-107">Parameters</span></span>

  - <span data-ttu-id="99fc7-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="99fc7-108">*pError*</span></span>

  - <span data-ttu-id="99fc7-p101">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si **adStatus** a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="99fc7-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="99fc7-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="99fc7-111">*adStatus*</span></span>

  - [<span data-ttu-id="99fc7-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="99fc7-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="99fc7-113">Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="99fc7-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="99fc7-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="99fc7-114">*pRecordset*</span></span>

  - <span data-ttu-id="99fc7-p102">Objet **Recordset** représentant le jeu duquel les enregistrements ont été extraits.</span><span class="sxs-lookup"><span data-stu-id="99fc7-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="99fc7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="99fc7-117">Remarks</span></span>

<span data-ttu-id="99fc7-118">Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchComplete** avec Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="99fc7-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

