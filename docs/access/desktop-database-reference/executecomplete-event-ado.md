---
title: ExecuteComplete, événement (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a094968e70ace5e6cba1df184bf0ba57c2d7789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293223"
---
# <a name="executecomplete-event-ado"></a><span data-ttu-id="dc557-102">ExecuteComplete, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="dc557-102">ExecuteComplete event (ADO)</span></span>

<span data-ttu-id="dc557-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc557-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc557-104">L'événement **ExecuteComplete** est appelé au terme de l'exécution d'une commande.</span><span class="sxs-lookup"><span data-stu-id="dc557-104">The **ExecuteComplete** event is called after a command has finished executing.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc557-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc557-105">Syntax</span></span>

<span data-ttu-id="dc557-106">ExecuteComplete*RecordsAffected*, *perror*, \*\* adStatus, *pCommand*, preobjet, \*\* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="dc557-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="dc557-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc557-107">Parameters</span></span>

|<span data-ttu-id="dc557-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc557-108">Parameter</span></span>|<span data-ttu-id="dc557-109">Description</span><span class="sxs-lookup"><span data-stu-id="dc557-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="dc557-110">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="dc557-110">*RecordsAffected*</span></span> |<span data-ttu-id="dc557-111">Valeur de type **Long** indiquant le nombre d'enregistrements affectés par la commande.</span><span class="sxs-lookup"><span data-stu-id="dc557-111">A **Long** value indicating the number of records affected by the command.</span></span>|
|<span data-ttu-id="dc557-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="dc557-112">*pError*</span></span> |<span data-ttu-id="dc557-p101">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si **adStatus** a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="dc557-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="dc557-115">*Statu*</span><span class="sxs-lookup"><span data-stu-id="dc557-115">*adStatus*</span></span> |<span data-ttu-id="dc557-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="dc557-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="dc557-117">Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dc557-117">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="dc557-118">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="dc557-118">*pCommand*</span></span> |<span data-ttu-id="dc557-p103">The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span><span class="sxs-lookup"><span data-stu-id="dc557-p103">The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span></span>|
|<span data-ttu-id="dc557-121">*jeu d'enregistrements*</span><span class="sxs-lookup"><span data-stu-id="dc557-121">*pRecordset*</span></span> |<span data-ttu-id="dc557-p104">Objet [Recordset](recordset-object-ado.md) résultant de la commande exécutée. Cet objet **Recordset** peut être vide. Il ne doit jamais être détruit à partir de ce gestionnaire d'événements. En effet, cela entraîne une violation d'accès puisqu'ADO tente d'accéder à un objet qui n'existe plus.</span><span class="sxs-lookup"><span data-stu-id="dc557-p104">A [Recordset](recordset-object-ado.md) object that is the result of the executed command. This **Recordset** may be empty. You should never destroy this Recordset object from within this event handler. Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</span></span>|
|<span data-ttu-id="dc557-126">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="dc557-126">*pConnection*</span></span> |<span data-ttu-id="dc557-p105">Objet [Connection](connection-object-ado.md), représentant la connexion utilisée pour l'exécution de l'opération.</span><span class="sxs-lookup"><span data-stu-id="dc557-p105">A [Connection](connection-object-ado.md) object. The connection over which the operation was executed.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dc557-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="dc557-129">Remarks</span></span>

<span data-ttu-id="dc557-130">Un événement **ExecuteComplete** peut se produire avec les méthodes **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) ou **Recordset.**[NextRecordset](nextrecordset-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dc557-130">An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>

