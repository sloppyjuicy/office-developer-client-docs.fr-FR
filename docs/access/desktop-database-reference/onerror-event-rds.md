---
title: onError, événement (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712175"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="4ebfe-102">onError, événement (RDS)</span><span class="sxs-lookup"><span data-stu-id="4ebfe-102">onError event (RDS)</span></span>

<span data-ttu-id="4ebfe-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ebfe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ebfe-104">L'événement **onError** est appelé chaque fois qu'une erreur se produit pendant une opération.</span><span class="sxs-lookup"><span data-stu-id="4ebfe-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebfe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ebfe-105">Syntax</span></span>

<span data-ttu-id="4ebfe-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="4ebfe-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="4ebfe-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4ebfe-107">Parameters</span></span>

|<span data-ttu-id="4ebfe-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="4ebfe-108">Parameter</span></span>|<span data-ttu-id="4ebfe-109">Description</span><span class="sxs-lookup"><span data-stu-id="4ebfe-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4ebfe-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="4ebfe-110">*SCode*</span></span> |<span data-ttu-id="4ebfe-111">Entier indiquant le code d'état de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="4ebfe-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="4ebfe-112">*Description*</span><span class="sxs-lookup"><span data-stu-id="4ebfe-112">*Description*</span></span> |<span data-ttu-id="4ebfe-113">Valeur de type **String** reprenant une description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="4ebfe-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="4ebfe-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="4ebfe-114">*Source*</span></span> |<span data-ttu-id="4ebfe-115">Valeur de type **String** indiquant la requête ou la commande à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="4ebfe-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="4ebfe-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="4ebfe-116">*CancelDisplay*</span></span> |<span data-ttu-id="4ebfe-117">Valeur de type **Boolean**. Si la valeur est **True**, l'erreur n'est pas affichée dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4ebfe-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

