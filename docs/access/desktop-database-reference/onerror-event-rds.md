---
title: onError, événement (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fe6f6b78297008e25e15dc17e243ae982a5ccf3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472207"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="64b02-102">onError, événement (RDS)</span><span class="sxs-lookup"><span data-stu-id="64b02-102">onError Event (RDS)</span></span>


<span data-ttu-id="64b02-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="64b02-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="64b02-104">L'événement **onError** est appelé chaque fois qu'une erreur se produit pendant une opération.</span><span class="sxs-lookup"><span data-stu-id="64b02-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64b02-105">Syntax</span></span>

<span data-ttu-id="64b02-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="64b02-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="64b02-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64b02-107">Parameters</span></span>

  - <span data-ttu-id="64b02-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="64b02-108">*SCode*</span></span>

  - <span data-ttu-id="64b02-109">Entier indiquant le code d'état de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="64b02-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="64b02-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="64b02-110">*Description*</span></span>

  - <span data-ttu-id="64b02-111">Valeur de type **String** reprenant une description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="64b02-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="64b02-112">*Source*</span><span class="sxs-lookup"><span data-stu-id="64b02-112">*Source*</span></span>

  - <span data-ttu-id="64b02-113">Valeur de type **String** indiquant la requête ou la commande à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="64b02-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="64b02-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="64b02-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="64b02-115">Valeur de type **Boolean**. Si la valeur est **True**, l'erreur n'est pas affichée dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="64b02-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

