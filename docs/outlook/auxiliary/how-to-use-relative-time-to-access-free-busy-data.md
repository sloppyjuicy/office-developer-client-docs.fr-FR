---
title: Utiliser l’heure relative pour accéder aux données de disponibilité
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: L’interface IFreeBusyData dans l’API de disponibilité utilise un concept de temps relative, qui est le nombre de minutes depuis le 1er janvier 1601, exprimée en temps universel (UTC) et est une valeur de type LONG.
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386935"
---
# <a name="use-relative-time-to-access-freebusy-data"></a><span data-ttu-id="e46dc-103">Utiliser l’heure relative pour accéder aux données de disponibilité</span><span class="sxs-lookup"><span data-stu-id="e46dc-103">Use relative time to access free/busy data</span></span>

<span data-ttu-id="e46dc-104">L’interface [IFreeBusyData](ifreebusydata.md) dans l’API de disponibilité utilise un concept de temps relative, qui est le nombre de minutes depuis le 1er janvier 1601, exprimée en temps universel (UTC) et est une valeur de type **LONG**.</span><span class="sxs-lookup"><span data-stu-id="e46dc-104">The [IFreeBusyData](ifreebusydata.md) interface in the Free/Busy API uses a concept of relative time, which is the number of minutes since January 1, 1601, expressed in Universal Time (UTC), and is a value of type **LONG**.</span></span> 
  
<span data-ttu-id="e46dc-105">Certaines valeurs de durée relative couramment utilisés sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e46dc-105">The following are some commonly used relative time values:</span></span>
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
<span data-ttu-id="e46dc-106">Utilisez les valeurs maximale et minimale heure relative ci-dessus pour vérifier que les valeurs d’heure relative sont valides.</span><span class="sxs-lookup"><span data-stu-id="e46dc-106">Use the preceding maximum and minimum relative time values to help verify that your relative time values are valid.</span></span>
  
<span data-ttu-id="e46dc-107">NTFS enregistre les heures de fichier en mode natif au format [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) , il peut s’avérer utile de l’exemple de code suivant permet de convertir l’heure relative vers et depuis **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="e46dc-107">Because NTFS records file times natively in [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) format, it might be handy to use the following code example to convert relative time to and from **FILETIME**.</span></span> 
  
```cpp
static const LONGLONG UnitsPerMinute = 600000000; 
static const LONGLONG UnitsPerHalfMinute = 300000000; 
void RTimeToFileTime(LONG rtime, FILETIME *pft) 
{ 
    Assert(pft != NULL); 
    ULARGE_INTEGER *puli = (ULARGE_INTEGER *)pft; 
    puli->QuadPart = rtime * UnitsPerMinute; 
} 
  
void FileTimeToRTime(FILETIME *pft, LONG* prtime) 
{ 
    Assert(pft != NULL); 
    Assert(prtime != NULL); 
 
    ULARGE_INTEGER uli = *(ULARGE_INTEGER *)pft; 
  
    uli.QuadPart += UnitsPerHalfMinute; 
    uli.QuadPart /= UnitsPerMinute; 
    *prtime = uli.LowPart; 
} 

```

## <a name="see-also"></a><span data-ttu-id="e46dc-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e46dc-108">See also</span></span>

- [<span data-ttu-id="e46dc-109">À propos de l’API Disponibilité</span><span class="sxs-lookup"><span data-stu-id="e46dc-109">About the Free/Busy API</span></span>](about-the-free-busy-api.md)
- [<span data-ttu-id="e46dc-110">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="e46dc-110">IFreeBusyData</span></span>](ifreebusydata.md)

