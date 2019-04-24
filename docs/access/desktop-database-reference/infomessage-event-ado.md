---
title: InfoMessage, événement (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 879d8e7b3733937687671a164f86dbb273cf7533
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291441"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="63242-102">InfoMessage, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="63242-102">InfoMessage event (ADO)</span></span>

<span data-ttu-id="63242-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63242-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63242-104">L'événement **InfoMessage** est appelé à chaque avertissement généré lors d'une opération **ConnectionEvent**.</span><span class="sxs-lookup"><span data-stu-id="63242-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="63242-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63242-105">Syntax</span></span>

<span data-ttu-id="63242-106">InfoMessage*perror*, \*\* adStatus, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="63242-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="63242-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63242-107">Parameters</span></span>

|<span data-ttu-id="63242-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="63242-108">Parameter</span></span>|<span data-ttu-id="63242-109">Description</span><span class="sxs-lookup"><span data-stu-id="63242-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="63242-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="63242-110">*pError*</span></span> |<span data-ttu-id="63242-p101">Objet [Error](error-object-ado.md). Ce paramètre contient toutes les erreurs générées lors de l'opération. Si plusieurs erreurs sont retournées, énumérez la collection **Errors** pour les identifier.</span><span class="sxs-lookup"><span data-stu-id="63242-p101">An [Error](error-object-ado.md) object. This parameter contains any errors that are returned. If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>|
|<span data-ttu-id="63242-114">*Statu*</span><span class="sxs-lookup"><span data-stu-id="63242-114">*adStatus*</span></span> |<span data-ttu-id="63242-115">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="63242-115">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="63242-116">Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="63242-116">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="63242-117">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="63242-117">*pConnection*</span></span> |<span data-ttu-id="63242-p103">Objet [Connection](connection-object-ado.md). Connexion pour laquelle l'avertissement a été émis. Par exemple, des avertissements peuvent être générés lors de l'ouverture d'un objet **Connection** ou pendant l'exécution d'un objet [Command](command-object-ado.md) sur un objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="63242-p103">A [Connection](connection-object-ado.md) object. The connection for which the warning occurred. For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>|

