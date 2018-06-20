---
title: Gestion d'événements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782123"
---
# <a name="handling-events"></a>Gestion d'événements

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
À compter d’Excel 2010, XLL peuvent recevoir des événements conçus pour gérer le cycle de vie de fonction asynchrone. Les événements sont les suivants :
  
- **CalculationEnded**: déclenché lors de la fin du calcul. Après cet événement, vous pouvez libérer les ressources allouées au cours du calcul.
    
- **CalculationCanceled**: déclenché lorsque l’utilisateur interrompt le calcul. La ressource XLL arrête toutes les activités asynchrones. Immédiatement après cet événement, l’événement **CalculationEnded** est déclenché. 
    
Pour gérer ces événements, le XLL utilise la fonction de API C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** et **CalculationCanceled** ne sont pas déclenchés lors d’un recalcul par programme. 
  

