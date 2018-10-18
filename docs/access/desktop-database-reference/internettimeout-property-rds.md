---
title: InternetTimeout, propriété (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd0fdc8f64207e1233ac56812ef009da865ce01a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603461"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="19afc-102">InternetTimeout, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="19afc-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="19afc-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="19afc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="19afc-104">Indique le nombre de millisecondes s'écoulant avant l'expiration d'une requête.</span><span class="sxs-lookup"><span data-stu-id="19afc-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

<span data-ttu-id="19afc-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="19afc-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="19afc-106">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="19afc-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="19afc-107">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="19afc-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="19afc-108">master</span><span class="sxs-lookup"><span data-stu-id="19afc-108">master</span></span>

<span data-ttu-id="19afc-109">Définit ou renvoie une valeur **Long** qui représente le nombre de millisecondes s'écoulant avant l'expiration d'une requête.</span><span class="sxs-lookup"><span data-stu-id="19afc-109">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="19afc-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="19afc-110">Remarks</span></span>

<span data-ttu-id="19afc-111">Cette propriété s'applique exclusivement aux requêtes envoyées avec les protocoles HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="19afc-111">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="19afc-p101">Dans un environnement à trois niveaux, l'exécution des requêtes peut prendre plusieurs minutes. Utilisez cette propriété pour accorder du temps supplémentaire pour aux requêtes longues.</span><span class="sxs-lookup"><span data-stu-id="19afc-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

