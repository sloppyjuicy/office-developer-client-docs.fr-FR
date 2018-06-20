---
title: À propos de l’API de Conversion MAPI MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 43ce3ecea6b80bace2bcc2bd333b5c1839514f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782854"
---
# <a name="about-the-mapi-mime-conversion-api"></a>À propos de l’API de Conversion MAPI MIME

  
  
**S’applique à**: Outlook 
  
Les API de Conversion MAPI MIME permet à des fournisseurs de messagerie convertir les objets MIME et les messages MAPI. Il fournit des définitions de constantes, les identificateurs de classe et les identificateurs d’interface comme indiqué dans [Une des constantes MAPI](mapi-constants.md). Fournisseurs de messagerie doivent co-créer une instance de **[IConverterSession](iconvertersessioniunknown.md)** en appelant la fonction **CoCreateInstance** . 
  

