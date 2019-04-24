---
title: ConnectionTimeout, propriété (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295701"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="739a2-102">ConnectionTimeout, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="739a2-102">ConnectionTimeout property (ADO)</span></span>


<span data-ttu-id="739a2-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="739a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="739a2-104">Indique le délai d'attente pour l'établissement d'une connexion avant l'abandon de la tentative et la génération d'une erreur.</span><span class="sxs-lookup"><span data-stu-id="739a2-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="739a2-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="739a2-105">Settings and return values</span></span>

<span data-ttu-id="739a2-106">Définit ou renvoie une valeur de type **Long** indiquant, en secondes, le délai d'attente pour l'ouverture d'une connexion.</span><span class="sxs-lookup"><span data-stu-id="739a2-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open.</span></span> <span data-ttu-id="739a2-107">La valeur par défaut est 15.</span><span class="sxs-lookup"><span data-stu-id="739a2-107">Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="739a2-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="739a2-108">Remarks</span></span>

<span data-ttu-id="739a2-p102">Utilisez la propriété **ConnectionTimeout** dans un objet [Connection](connection-object-ado.md) si des retards dus au trafic réseau ou à une utilisation intensive du serveur imposent d'abandonner une tentative de connexion. Si le délai défini dans la propriété **ConnectionTimeout** s'écoule avant l'ouverture de la connexion, une erreur est générée et ADO annule la tentative. Si vous attribuez la valeur zéro à la propriété, ADO attend indéfiniment jusqu'à ce que la connexion soit ouverte. Assurez-vous que le fournisseur dans lequel vous écrivez le code prend en charge la fonctionnalité **ConnectionTimeout**.</span><span class="sxs-lookup"><span data-stu-id="739a2-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="739a2-113">La propriété **ConnectionTimeout** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte.</span><span class="sxs-lookup"><span data-stu-id="739a2-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

