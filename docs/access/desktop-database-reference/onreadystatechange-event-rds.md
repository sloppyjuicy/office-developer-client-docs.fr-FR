---
title: onReadyStateChange, événement (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dec783aaa76745b73bd031b00f1b8587a58eb165
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471270"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="30db8-102">onReadyStateChange, événement (RDS)</span><span class="sxs-lookup"><span data-stu-id="30db8-102">onReadyStateChange Event (RDS)</span></span>


<span data-ttu-id="30db8-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="30db8-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="30db8-104">L'événement **onReadyStateChange** est appelé chaque fois que la valeur de la propriété [ReadyState](readystate-property-rds.md) est modifiée.</span><span class="sxs-lookup"><span data-stu-id="30db8-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="30db8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30db8-105">Syntax</span></span>

<span data-ttu-id="30db8-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="30db8-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="30db8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30db8-107">Parameters</span></span>

<span data-ttu-id="30db8-108">Aucun.</span><span class="sxs-lookup"><span data-stu-id="30db8-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="30db8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="30db8-109">Remarks</span></span>

<span data-ttu-id="30db8-p101">La propriété **ReadyState** reflète la progression de l'opération de récupération des données asynchrone effectuée par un objet [RDS.DataControl](datacontrol-object-rds.md) dans son objet [Recordset](recordset-object-ado.md). L'événement **onReadyStateChange** permet de suivre les modifications apportées à la propriété **ReadyState**. Cette méthode s'avère plus efficace qu'un contrôle périodique de la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="30db8-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

