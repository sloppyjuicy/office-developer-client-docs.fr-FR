---
title: Fonctions du connecteur de cluster Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408585"
---
# <a name="excel-cluster-connector-functions"></a><span data-ttu-id="ff243-103">Fonctions du connecteur de cluster Excel</span><span class="sxs-lookup"><span data-stu-id="ff243-103">Excel Cluster Connector Functions</span></span>

 <span data-ttu-id="ff243-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ff243-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ff243-105">Les dll de connecteur de cluster Microsoft Excel 2013 doivent implémenter les fonctions décrites dans cette section.</span><span class="sxs-lookup"><span data-stu-id="ff243-105">Microsoft Excel 2013 cluster connector DLLs must implement the functions described in this section.</span></span>
  
<span data-ttu-id="ff243-106">Les valeurs renvoyées mentionnées dans les rubriques de référence de cette section sont définies dans le fichier include SDK xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="ff243-106">The return values mentioned in reference topics in this section are defined in the SDK include file, xlcall.h.</span></span>
  
## <a name="cluster-connector-architecture"></a><span data-ttu-id="ff243-107">Architecture de connecteur de cluster</span><span class="sxs-lookup"><span data-stu-id="ff243-107">Cluster Connector Architecture</span></span>

<span data-ttu-id="ff243-108">Excel appelle les points d'entrée dans un connecteur de cluster pour transférer les appels de fonction définis par l'utilisateur vers un cluster de calcul à hautes performances et pour la gestion de session de cluster.</span><span class="sxs-lookup"><span data-stu-id="ff243-108">Excel calls entry points in a cluster connector to transfer user-defined function calls to a high-performance compute cluster, and for cluster session management.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="ff243-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ff243-109">In this section</span></span>

[<span data-ttu-id="ff243-110">CallUDF</span><span class="sxs-lookup"><span data-stu-id="ff243-110">CallUDF</span></span>](calludf.md)
  
[<span data-ttu-id="ff243-111">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="ff243-111">CancelOutstandingRequests</span></span>](canceloutstandingrequests.md)
  
[<span data-ttu-id="ff243-112">CloseSession</span><span class="sxs-lookup"><span data-stu-id="ff243-112">CloseSession</span></span>](closesession.md)
  
[<span data-ttu-id="ff243-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="ff243-113">OpenSession</span></span>](opensession.md)
  
[<span data-ttu-id="ff243-114">PingSession</span><span class="sxs-lookup"><span data-stu-id="ff243-114">PingSession</span></span>](pingsession.md)
  
[<span data-ttu-id="ff243-115">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="ff243-115">ShowOptions</span></span>](showoptions.md)
  
## <a name="see-also"></a><span data-ttu-id="ff243-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff243-116">See also</span></span>



[<span data-ttu-id="ff243-117">D�veloppement de connecteurs de Cluster Excel 2013</span><span class="sxs-lookup"><span data-stu-id="ff243-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
  
[<span data-ttu-id="ff243-118">Fonctions sécurisées pour le cluster</span><span class="sxs-lookup"><span data-stu-id="ff243-118">Cluster Safe Functions</span></span>](cluster-safe-functions.md)

