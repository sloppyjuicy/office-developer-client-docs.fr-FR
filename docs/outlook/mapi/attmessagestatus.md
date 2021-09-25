---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ce34b9b3b3c2f8a3a3f6814507225145eb39d86b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564433"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les indicateurs de message MAPI sont mappés aux indicateurs TNEF pour préserver la compatibilité ascendante. Tous les indicateurs sont regroupés et codés dans un seul et même byte. Les mappages sont les suivants :
  
|**Indicateurs de message MAPI**|**Indicateurs TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Ces indicateurs sont définis dans le TNEF. Fichier d’en-tête H.
  

