---
title: InfoMessage, événement (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1db793ec99dd0248eacc527bd76068ceec025a58
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949431"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="8cda4-102">InfoMessage, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="8cda4-102">InfoMessage event (ADO)</span></span>

<span data-ttu-id="8cda4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8cda4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8cda4-104">L'événement **InfoMessage** est appelé à chaque avertissement généré lors d'une opération **ConnectionEvent**.</span><span class="sxs-lookup"><span data-stu-id="8cda4-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cda4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cda4-105">Syntax</span></span>

<span data-ttu-id="8cda4-106">InfoMessage*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="8cda4-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="8cda4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cda4-107">Parameters</span></span>

|<span data-ttu-id="8cda4-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8cda4-108">Parameter</span></span>|<span data-ttu-id="8cda4-109">Description</span><span class="sxs-lookup"><span data-stu-id="8cda4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8cda4-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="8cda4-110">*pError*</span></span> |<span data-ttu-id="8cda4-p101">Objet [Error](error-object-ado.md). Ce paramètre contient toutes les erreurs générées lors de l'opération. Si plusieurs erreurs sont retournées, énumérez la collection **Errors** pour les identifier.</span><span class="sxs-lookup"><span data-stu-id="8cda4-p101">An [Error](error-object-ado.md) object. This parameter contains any errors that are returned. If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>|
|<span data-ttu-id="8cda4-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="8cda4-114">*adStatus*</span></span> |<span data-ttu-id="8cda4-115">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="8cda4-115">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="8cda4-116">Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8cda4-116">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="8cda4-117">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="8cda4-117">*pConnection*</span></span> |<span data-ttu-id="8cda4-p103">Objet [Connection](connection-object-ado.md). Connexion pour laquelle l'avertissement a été émis. Par exemple, des avertissements peuvent être générés lors de l'ouverture d'un objet **Connection** ou pendant l'exécution d'un objet [Command](command-object-ado.md) sur un objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="8cda4-p103">A [Connection](connection-object-ado.md) object. The connection for which the warning occurred. For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>|

