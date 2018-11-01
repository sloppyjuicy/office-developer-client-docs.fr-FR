---
title: InternetTimeout, propriété (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06e844b9e6e0976679820fbc2ac79eae14131d36
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879042"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="a93c1-102">InternetTimeout, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="a93c1-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="a93c1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a93c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a93c1-104">Indique le nombre de millisecondes s'écoulant avant l'expiration d'une requête.</span><span class="sxs-lookup"><span data-stu-id="a93c1-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a93c1-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a93c1-105">Settings and return values</span></span>

<span data-ttu-id="a93c1-106">Définit ou renvoie une valeur **Long** qui représente le nombre de millisecondes s'écoulant avant l'expiration d'une requête.</span><span class="sxs-lookup"><span data-stu-id="a93c1-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="a93c1-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="a93c1-107">Remarks</span></span>

<span data-ttu-id="a93c1-108">Cette propriété s'applique exclusivement aux requêtes envoyées avec les protocoles HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a93c1-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="a93c1-p101">Dans un environnement à trois niveaux, l'exécution des requêtes peut prendre plusieurs minutes. Utilisez cette propriété pour accorder du temps supplémentaire pour aux requêtes longues.</span><span class="sxs-lookup"><span data-stu-id="a93c1-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

