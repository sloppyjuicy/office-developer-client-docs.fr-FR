---
title: Éviter d’utiliser IStreamSetSize pour étendre un flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
ms.openlocfilehash: 5310a52169456499b9fcde2787fd491356517b50
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371729"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Éviter d’utiliser IStream::SetSize pour étendre un flux

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l’écriture dans des flux, il est parfois nécessaire de les agrandir, car leur taille initiale n’est plus suffisante. Utilisez la méthode OLE **IStream::Write** pour effectuer cette tâche plutôt que **IStream::SetSize**. **IStream::Write** étend automatiquement le flux, ce qui rend ** IStream::SetSize ** inutile. Appeler **IStream::Write** sans **IStream::SetSize** peut être jusqu’à trois fois plus rapide que d’effectuer l’appel **SetSize** avant **d’écrire**.
  

