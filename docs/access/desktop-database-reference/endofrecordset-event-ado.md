---
title: EndOfRecordset, événement (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721359"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="a550c-102">EndOfRecordset, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="a550c-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="a550c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a550c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a550c-104">L'événement **EndOfRecordset** est appelé lors d'une tentative de positionnement sur une ligne au-delà de la fin d'un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a550c-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a550c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a550c-105">Syntax</span></span>

<span data-ttu-id="a550c-106">EndOfRecordset*fMoreData*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="a550c-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="a550c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a550c-107">Parameters</span></span>

|<span data-ttu-id="a550c-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a550c-108">Parameter</span></span>|<span data-ttu-id="a550c-109">Description</span><span class="sxs-lookup"><span data-stu-id="a550c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a550c-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="a550c-110">*fMoreData*</span></span> |<span data-ttu-id="a550c-111">A **VARIANT\_BOOL** valeur de la valeur de type VARIANT\_la valeur TRUE, indique plus de lignes qui ont été ajoutés au **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="a550c-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="a550c-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="a550c-112">*adStatus*</span></span> |<span data-ttu-id="a550c-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="a550c-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="a550c-114">Lorsque **EndOfRecordset** est appelé, ce paramètre a la valeur **adStatusOK** si l’opération qui a provoqué l’événement a réussi.</span><span class="sxs-lookup"><span data-stu-id="a550c-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="a550c-115">Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l’annulation de l’opération qui a provoqué l’événement.</span><span class="sxs-lookup"><span data-stu-id="a550c-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="a550c-116">Avant que **EndOfRecordset** ne soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre afin d'empêcher toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a550c-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="a550c-117">*Connection*</span><span class="sxs-lookup"><span data-stu-id="a550c-117">*pRecordset*</span></span> | <span data-ttu-id="a550c-118">Objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a550c-118">A **Recordset** object.</span></span> <span data-ttu-id="a550c-119">Le **jeu d’enregistrements** pour laquelle cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="a550c-119">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a550c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a550c-120">Remarks</span></span>

<span data-ttu-id="a550c-121">Un événement **EndOfRecordset** peut être généré si l'opération [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) échoue.</span><span class="sxs-lookup"><span data-stu-id="a550c-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="a550c-122">Ce gestionnaire d'événements est appelé lors d'une tentative de positionnement au-delà de la fin de l'objet **Recordset**, résultant probablement d'un appel à **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="a550c-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="a550c-123">À partir de l'événement, il est toujours possible toutefois de récupérer plusieurs enregistrements d'une base de données et de les ajouter à la fin de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a550c-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="a550c-124">Dans ce cas, la valeur de type VARIANT *fMoreData* \_la valeur TRUE et de retour à partir de **l’événement EndOfRecordset**.</span><span class="sxs-lookup"><span data-stu-id="a550c-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="a550c-125">Rappelez ensuite **MoveNext** pour accéder aux nouveaux enregistrements récupérés.</span><span class="sxs-lookup"><span data-stu-id="a550c-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

