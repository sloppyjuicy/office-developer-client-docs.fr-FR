---
title: onError, événement (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c67e277c35e3cf6c75226dc138aa4b288843e6bf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930860"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="d2c7e-102">onError, événement (RDS)</span><span class="sxs-lookup"><span data-stu-id="d2c7e-102">onError event (RDS)</span></span>


<span data-ttu-id="d2c7e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2c7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2c7e-104">L'événement **onError** est appelé chaque fois qu'une erreur se produit pendant une opération.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2c7e-105">Syntax</span></span>

<span data-ttu-id="d2c7e-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="d2c7e-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="d2c7e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2c7e-107">Parameters</span></span>

  - <span data-ttu-id="d2c7e-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="d2c7e-108">*SCode*</span></span>

  - <span data-ttu-id="d2c7e-109">Entier indiquant le code d'état de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="d2c7e-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="d2c7e-110">*Description*</span></span>

  - <span data-ttu-id="d2c7e-111">Valeur de type **String** reprenant une description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="d2c7e-112">*Source*</span><span class="sxs-lookup"><span data-stu-id="d2c7e-112">*Source*</span></span>

  - <span data-ttu-id="d2c7e-113">Valeur de type **String** indiquant la requête ou la commande à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="d2c7e-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="d2c7e-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="d2c7e-115">Valeur de type **Boolean**. Si la valeur est **True**, l'erreur n'est pas affichée dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d2c7e-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

