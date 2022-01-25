---
title: Gestion d'événements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
ms.openlocfilehash: dd4cdab899a77647bc8216edcafd4776baf0d677
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199317"
---
# <a name="handling-events"></a>Gestion d'événements

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
À compter Excel 2010, les XL peuvent recevoir des événements conçus pour gérer le cycle de vie de la fonction asynchrone. Les événements sont les suivants :
  
- **CalculationEnded**: élevé lorsque Excel est terminé le calcul. Après cet événement, vous pouvez libérer les ressources allouées pendant le calcul.
    
- **CalculationCanceled :** élevé lorsque l’utilisateur interrompt le calcul. Le XLL arrête toutes les activités asynchrones. Immédiatement après cet événement, **l’événement CalculationEnded** est lancé. 
    
Pour gérer ces événements, le XLL utilise la fonction API C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded et** **CalculationCanceled** ne sont pas élevés lors du recalcul par programme. 
  

