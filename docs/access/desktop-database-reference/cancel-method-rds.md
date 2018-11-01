---
title: Cancel, méthode (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8455496e8d426d26f56b902d9a089d236bde1a6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868744"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="b139e-102">Cancel, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="b139e-102">Cancel Method (RDS)</span></span>


<span data-ttu-id="b139e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b139e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b139e-104">Annule l'exécution d'un appel de méthode asynchrone en attente.</span><span class="sxs-lookup"><span data-stu-id="b139e-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="b139e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b139e-105">Syntax</span></span>

<span data-ttu-id="b139e-106">*RDS*.</span><span class="sxs-lookup"><span data-stu-id="b139e-106">*RDS*.</span></span> <span data-ttu-id="b139e-107">*DataControl*. Annuler</span><span class="sxs-lookup"><span data-stu-id="b139e-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="b139e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="b139e-108">Remarks</span></span>

<span data-ttu-id="b139e-109">Lorsque vous appelez **Cancel**, [ReadyState](readystate-property-rds.md) prend automatiquement la valeur **adcReadyStateLoaded** et l'objet [Recordset](recordset-object-ado.md) sera vide.</span><span class="sxs-lookup"><span data-stu-id="b139e-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

