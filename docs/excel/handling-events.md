---
title: Gestion d'événements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304038"
---
# <a name="handling-events"></a>Gestion d'événements

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
À partir d'Excel 2010, les XLL peuvent recevoir des événements conçus pour gérer le cycle de vie des fonctions asynchrones. Les événements sont les suivants:
  
- **CalculationEnded**: déclenché une fois que le calcul d'Excel est terminé. Après cet événement, vous pouvez libérer les ressources allouées pendant le calcul.
    
- **CalculationCanceled**: déclenché lorsque l'utilisateur interrompt le calcul. Le XLL arrête toutes les activités asynchrones. Immédiatement après cet événement, l'événement **CalculationEnded** est déclenché. 
    
Pour gérer ces événements, la XLL utilise la fonction API C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** et **CalculationCanceled** ne sont pas déclenchés lors du recalcul de programmation. 
  

