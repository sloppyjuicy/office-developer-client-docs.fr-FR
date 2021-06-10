---
title: InternetTimeout, propriété (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291240"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="9dd6f-102">InternetTimeout, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="9dd6f-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="9dd6f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9dd6f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9dd6f-104">Indique le nombre de millisecondes s'écoulant avant l'expiration d'une requête.</span><span class="sxs-lookup"><span data-stu-id="9dd6f-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="9dd6f-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="9dd6f-105">Settings and return values</span></span>

<span data-ttu-id="9dd6f-106">Définit ou renvoie une valeur **Long** qui représente le nombre de millisecondes s'écoulant avant l'expiration d'une requête.</span><span class="sxs-lookup"><span data-stu-id="9dd6f-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd6f-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="9dd6f-107">Remarks</span></span>

<span data-ttu-id="9dd6f-108">Cette propriété s'applique exclusivement aux requêtes envoyées avec les protocoles HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9dd6f-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="9dd6f-p101">Dans un environnement à trois niveaux, l'exécution des requêtes peut prendre plusieurs minutes. Utilisez cette propriété pour accorder du temps supplémentaire pour aux requêtes longues.</span><span class="sxs-lookup"><span data-stu-id="9dd6f-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

