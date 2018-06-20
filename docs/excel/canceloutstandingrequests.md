---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782011"
---
# <a name="canceloutstandingrequests"></a><span data-ttu-id="19118-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="19118-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="19118-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="19118-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="19118-105">Informe le connecteur de cluster un calcul Excel a été annulé, et par conséquent, tout en attente d’appels de fonction au sein de cette session peut être annulée ainsi (et que Microsoft Excel n’attend pas de rappels avec leurs résultats).</span><span class="sxs-lookup"><span data-stu-id="19118-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="19118-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19118-106">Parameters</span></span>

<span data-ttu-id="19118-107">_ID de session_</span><span class="sxs-lookup"><span data-stu-id="19118-107">_SessionID_</span></span>
  
> <span data-ttu-id="19118-108">ID de la session utilisée par le calcul annulé.</span><span class="sxs-lookup"><span data-stu-id="19118-108">The ID of the session used by the canceled calculation.</span></span> <span data-ttu-id="19118-109">Cette valeur correspond à la valeur renvoyée par la [méthode OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="19118-109">This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="19118-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="19118-110">Return value</span></span>

<span data-ttu-id="19118-111">**xlHpcRetSuccess** si l’argument _SessionId_ est valide ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed** sur les autres erreurs.</span><span class="sxs-lookup"><span data-stu-id="19118-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="19118-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="19118-112">Remarks</span></span>

<span data-ttu-id="19118-113">L’implémentation doit s’arrêter tous les processus pour la session pour améliorer les performances, en tant que les résultats reçus après que cet appel est ignoré par Excel.</span><span class="sxs-lookup"><span data-stu-id="19118-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19118-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19118-114">See also</span></span>

- [<span data-ttu-id="19118-115">Fonctions du connecteur de Cluster Excel</span><span class="sxs-lookup"><span data-stu-id="19118-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

