---
title: onError, événement (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17cbeece67ffa19666f6209a38159c9a2c6a44ea
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889944"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="89fe1-102">onError, événement (RDS)</span><span class="sxs-lookup"><span data-stu-id="89fe1-102">onError Event (RDS)</span></span>


<span data-ttu-id="89fe1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89fe1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89fe1-104">L'événement **onError** est appelé chaque fois qu'une erreur se produit pendant une opération.</span><span class="sxs-lookup"><span data-stu-id="89fe1-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fe1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89fe1-105">Syntax</span></span>

<span data-ttu-id="89fe1-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="89fe1-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="89fe1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89fe1-107">Parameters</span></span>

  - <span data-ttu-id="89fe1-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="89fe1-108">*SCode*</span></span>

  - <span data-ttu-id="89fe1-109">Entier indiquant le code d'état de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="89fe1-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="89fe1-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="89fe1-110">*Description*</span></span>

  - <span data-ttu-id="89fe1-111">Valeur de type **String** reprenant une description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="89fe1-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="89fe1-112">*Source*</span><span class="sxs-lookup"><span data-stu-id="89fe1-112">*Source*</span></span>

  - <span data-ttu-id="89fe1-113">Valeur de type **String** indiquant la requête ou la commande à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="89fe1-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="89fe1-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="89fe1-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="89fe1-115">Valeur de type **Boolean**. Si la valeur est **True**, l'erreur n'est pas affichée dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="89fe1-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

