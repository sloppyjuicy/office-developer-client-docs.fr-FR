---
title: Gestion d'événements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0576687d6bb80f6fc3d5779db3625beccbfbc28c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572395"
---
# <a name="handling-events"></a>Gestion d'événements

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
À compter Excel 2010, les XL peuvent recevoir des événements conçus pour gérer le cycle de vie de la fonction asynchrone. Les événements sont les suivants :
  
- **CalculationEnded**: élevé lorsque Excel est terminé le calcul. Après cet événement, vous pouvez libérer les ressources allouées pendant le calcul.
    
- **CalculationCanceled :** élevé lorsque l’utilisateur interrompt le calcul. Le XLL arrête toutes les activités asynchrones. Immédiatement après cet événement, **l’événement CalculationEnded** est lancé. 
    
Pour gérer ces événements, le XLL utilise la fonction API C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded et** **CalculationCanceled** ne sont pas élevés lors du recalcul par programme. 
  

