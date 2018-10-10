---
title: ConnectionTimeout, propriété (ADO)
TOCTitle: ConnectionTimeout Property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 375af7f4dc84d1a630c290df1c38e77ee6580b5d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470346"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="ef1e7-102">ConnectionTimeout, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="ef1e7-102">ConnectionTimeout Property (ADO)</span></span>


<span data-ttu-id="ef1e7-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef1e7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ef1e7-104">Indique le délai d'attente pour l'établissement d'une connexion avant l'abandon de la tentative et la génération d'une erreur.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ef1e7-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ef1e7-105">Settings and Return Values</span></span>

<span data-ttu-id="ef1e7-p101">Définit ou renvoie une valeur de type **Long** indiquant, en secondes, le délai d'attente pour l'ouverture d'une connexion. La valeur par défaut est 15.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-p101">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open. Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1e7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ef1e7-108">Remarks</span></span>

<span data-ttu-id="ef1e7-p102">Utilisez la propriété **ConnectionTimeout** dans un objet [Connection](connection-object-ado.md) si des retards dus au trafic réseau ou à une utilisation intensive du serveur imposent d'abandonner une tentative de connexion. Si le délai défini dans la propriété **ConnectionTimeout** s'écoule avant l'ouverture de la connexion, une erreur est générée et ADO annule la tentative. Si vous attribuez la valeur zéro à la propriété, ADO attend indéfiniment jusqu'à ce que la connexion soit ouverte. Assurez-vous que le fournisseur dans lequel vous écrivez le code prend en charge la fonctionnalité **ConnectionTimeout**.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="ef1e7-113">La propriété **ConnectionTimeout** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte.</span><span class="sxs-lookup"><span data-stu-id="ef1e7-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

