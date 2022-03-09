---
title: À propos de l’API de conversion MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
ms.openlocfilehash: 299ef485861fe9b092786a2834de85d87e2bb8f5
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379814"
---
# <a name="about-the-mapi-mime-conversion-api"></a>À propos de l’API de conversion MAPI-MIME

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API de conversion MAPI-MIME permet aux fournisseurs de messagerie de convertir entre des objets MIME et des messages MAPI. Il fournit des définitions de constantes, des identificateurs de classe et des identificateurs d’interface, comme indiqué dans les [constantes MAPI](mapi-constants.md). Les fournisseurs de messagerie doivent cocréer une instance **[d’IConverterSession](iconvertersessioniunknown.md)** en appelant la fonction **CoCreateInstance** . 
  

