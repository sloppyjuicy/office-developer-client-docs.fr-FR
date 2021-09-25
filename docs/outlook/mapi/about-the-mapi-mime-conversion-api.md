---
title: À propos de l’API de conversion MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c36dd3e6761c5bb63fe6560bfa332d1b0548b689
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567927"
---
# <a name="about-the-mapi-mime-conversion-api"></a>À propos de l’API de conversion MAPI-MIME

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API de conversion MAPI-MIME permet aux fournisseurs de messagerie de convertir entre des objets MIME et des messages MAPI. Il fournit des définitions de constantes, des identificateurs de classe et des identificateurs d’interface, comme indiqué dans les [constantes MAPI.](mapi-constants.md) Les fournisseurs de messagerie doivent cocréer une instance **[d’IConverterSession](iconvertersessioniunknown.md)** en appelant la fonction **CoCreateInstance.** 
  

