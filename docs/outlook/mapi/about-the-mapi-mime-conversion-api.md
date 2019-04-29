---
title: À propos de l’API de conversion MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420436"
---
# <a name="about-the-mapi-mime-conversion-api"></a>À propos de l’API de conversion MAPI-MIME

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'API de conversion MAPI-MIME permet aux fournisseurs de courrier de convertir les objets MIME et les messages MAPI. Elle fournit des définitions, des identificateurs de classe et des identificateurs d'interface constants, comme indiqué dans les [constantes MAPI](mapi-constants.md). Les fournisseurs de messagerie doivent créer une instance de **[IConverterSession](iconvertersessioniunknown.md)** en appelant la fonction **CoCreateInstance** . 
  

