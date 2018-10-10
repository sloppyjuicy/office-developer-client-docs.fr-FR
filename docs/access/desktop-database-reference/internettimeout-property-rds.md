---
title: InternetTimeout, propriété (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929b166a308276836fbe4a48a2461ef7eb0caba2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469103"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="75461-102">InternetTimeout, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="75461-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="75461-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75461-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75461-104">Indique le nombre de millisecondes s'écoulant avant l'expiration d'une requête.</span><span class="sxs-lookup"><span data-stu-id="75461-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="75461-105">Paramètres et valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="75461-105">Settings and Return Values</span></span>

<span data-ttu-id="75461-106">Définit ou renvoie une valeur **Long** qui représente le nombre de millisecondes s'écoulant avant l'expiration d'une requête.</span><span class="sxs-lookup"><span data-stu-id="75461-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="75461-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="75461-107">Remarks</span></span>

<span data-ttu-id="75461-108">Cette propriété s'applique exclusivement aux requêtes envoyées avec les protocoles HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="75461-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="75461-p101">Dans un environnement à trois niveaux, l'exécution des requêtes peut prendre plusieurs minutes. Utilisez cette propriété pour accorder du temps supplémentaire pour aux requêtes longues.</span><span class="sxs-lookup"><span data-stu-id="75461-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

