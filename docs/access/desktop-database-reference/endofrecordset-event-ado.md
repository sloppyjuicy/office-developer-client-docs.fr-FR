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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293559"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="f44df-102">EndOfRecordset, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="f44df-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="f44df-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f44df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f44df-104">L’événement **EndOfRecordset** est appelé lors d’une tentative de positionnement sur une ligne au-delà de la fin d’un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f44df-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f44df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f44df-105">Syntax</span></span>

<span data-ttu-id="f44df-106">EndOfRecordset*fMoreData*, \*\* adStatus, *Recordset*</span><span class="sxs-lookup"><span data-stu-id="f44df-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="f44df-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f44df-107">Parameters</span></span>

|<span data-ttu-id="f44df-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f44df-108">Parameter</span></span>|<span data-ttu-id="f44df-109">Description</span><span class="sxs-lookup"><span data-stu-id="f44df-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f44df-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="f44df-110">*fMoreData*</span></span> |<span data-ttu-id="f44df-111">Valeur **de\_type Variant bool** qui, si elle est\_définie sur la valeur variant true, indique que des lignes supplémentaires ont été ajoutées à l' **objet Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f44df-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="f44df-112">*Statu*</span><span class="sxs-lookup"><span data-stu-id="f44df-112">*adStatus*</span></span> |<span data-ttu-id="f44df-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="f44df-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="f44df-114">Lorsque **EndOfRecordset** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement.</span><span class="sxs-lookup"><span data-stu-id="f44df-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="f44df-115">Elle est définie sur **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération à l'origine de l'événement.</span><span class="sxs-lookup"><span data-stu-id="f44df-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="f44df-116">Avant que **EndOfRecordset** ne soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre afin d'empêcher toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f44df-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="f44df-117">*jeu d'enregistrements*</span><span class="sxs-lookup"><span data-stu-id="f44df-117">*pRecordset*</span></span> | <span data-ttu-id="f44df-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span><span class="sxs-lookup"><span data-stu-id="f44df-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f44df-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f44df-120">Remarks</span></span>

<span data-ttu-id="f44df-121">Un événement **EndOfRecordset** peut être généré si l'opération [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) échoue.</span><span class="sxs-lookup"><span data-stu-id="f44df-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="f44df-122">Ce gestionnaire d'événements est appelé lors d'une tentative de positionnement au-delà de la fin de l'objet **Recordset**, résultant probablement d'un appel à **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="f44df-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="f44df-123">À partir de l'événement, il est toujours possible toutefois de récupérer plusieurs enregistrements d'une base de données et de les ajouter à la fin de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f44df-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="f44df-124">Dans ce cas, affectez la valeur\_variant true à *fMoreData* et le retour à partir de **EndOfRecordset**.</span><span class="sxs-lookup"><span data-stu-id="f44df-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="f44df-125">Rappelez ensuite **MoveNext** pour accéder aux nouveaux enregistrements récupérés.</span><span class="sxs-lookup"><span data-stu-id="f44df-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

