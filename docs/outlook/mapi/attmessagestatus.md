---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565745"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Indicateurs de message MAPI sont mappés aux indicateurs TNEF pour conserver la compatibilité descendante. Tous les indicateurs sont groupées et codés à un octet. Les mappages sont les suivantes :
  
|**Indicateurs de message MAPI**|**Indicateurs TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~ fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Ces indicateurs sont définis dans le format TNEF. Fichier d’en-tête H.
  

