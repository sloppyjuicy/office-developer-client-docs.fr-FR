---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782967"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**S’applique à**: Outlook 
  
Indicateurs de message MAPI sont mappés aux indicateurs TNEF pour conserver la compatibilité descendante. Tous les indicateurs sont groupées et codés à un octet. Les mappages sont les suivantes :
  
|**Indicateurs de message MAPI**|**Indicateurs TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Ces indicateurs sont définis dans le format TNEF. Fichier d’en-tête H.
  

