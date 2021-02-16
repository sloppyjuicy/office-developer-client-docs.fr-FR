---
title: Éviter d’utiliser IStreamSetSize pour étendre un flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428913"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Éviter d’utiliser IStream::SetSize pour étendre un flux

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l’écriture dans des flux, il est parfois nécessaire de les agrandir, car leur taille initiale n’est plus suffisante. Utilisez la méthode OLE **IStream::Write** pour effectuer cette tâche plutôt que **IStream::SetSize**. **IStream::Write** étend automatiquement le flux, ce qui rend ** IStream::SetSize ** inutile. Appeler **IStream::Write** sans **IStream::SetSize** peut être jusqu’à trois fois plus rapide que d’effectuer l’appel **SetSize** avant d’écrire. 
  

