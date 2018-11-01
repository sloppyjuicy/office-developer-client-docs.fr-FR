---
title: onReadyStateChange, événement (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bea7d7ae5a7fe0681af315c8569bf9b67d8bd82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869231"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="12c21-102">onReadyStateChange, événement (RDS)</span><span class="sxs-lookup"><span data-stu-id="12c21-102">onReadyStateChange Event (RDS)</span></span>


<span data-ttu-id="12c21-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12c21-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="12c21-104">L'événement **onReadyStateChange** est appelé chaque fois que la valeur de la propriété [ReadyState](readystate-property-rds.md) est modifiée.</span><span class="sxs-lookup"><span data-stu-id="12c21-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c21-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12c21-105">Syntax</span></span>

<span data-ttu-id="12c21-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="12c21-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="12c21-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12c21-107">Parameters</span></span>

<span data-ttu-id="12c21-108">Aucun.</span><span class="sxs-lookup"><span data-stu-id="12c21-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="12c21-109">Notes</span><span class="sxs-lookup"><span data-stu-id="12c21-109">Remarks</span></span>

<span data-ttu-id="12c21-p101">La propriété **ReadyState** reflète la progression de l'opération de récupération des données asynchrone effectuée par un objet [RDS.DataControl](datacontrol-object-rds.md) dans son objet [Recordset](recordset-object-ado.md). L'événement **onReadyStateChange** permet de suivre les modifications apportées à la propriété **ReadyState**. Cette méthode s'avère plus efficace qu'un contrôle périodique de la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="12c21-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

