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
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318213"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les indicateurs de message MAPI sont mappés aux indicateurs TNEF pour conserver la compatibilité descendante. Tous les indicateurs sont regroupés et codés en un seul octet. Les mappages sont les suivants:
  
|**Indicateurs de message MAPI**|**Indicateurs TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Ces indicateurs sont définis dans le format TNEF. Fichier d'en-tête H.
  

