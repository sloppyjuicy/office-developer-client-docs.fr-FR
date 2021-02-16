---
title: Gestion d'événements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438266"
---
# <a name="handling-events"></a>Gestion d'événements

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
À partir d’Excel 2010, les XL peuvent recevoir des événements conçus pour gérer le cycle de vie de la fonction asynchrone. Les événements sont les suivants :
  
- **CalculationEnded :** élevé lorsque Excel a terminé le calcul. Après cet événement, vous pouvez libérer les ressources allouées pendant le calcul.
    
- **CalculationCanceled :** élevé lorsque l’utilisateur interrompt le calcul. Le XLL arrête toutes les activités asynchrones. Immédiatement après cet événement, **l’événement CalculationEnded** est lancé. 
    
Pour gérer ces événements, le XLL utilise la fonction API C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded et** **CalculationCanceled** ne sont pas élevés lors du recalcul par programme. 
  

