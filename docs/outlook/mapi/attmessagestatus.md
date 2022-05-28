---
title: attMessageStatus
description: Décrit l’attribut MessageStatus et fournit une liste de messages MAPI et d’indicateurs TNEF.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
ms.openlocfilehash: fa1fa7942a2ccfffdecafdb022fb25595bc9c0f3
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769976"
---
# <a name="attmessagestatus"></a>attMessageStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les indicateurs de message MAPI sont mappés aux indicateurs TNEF pour préserver la compatibilité descendante. Tous les indicateurs sont regroupés et encodés en un seul octet. Les mappages sont les suivants :
  
|**Indicateurs de message MAPI**|**Indicateurs TNEF**|
|:-----|:-----|
|MSGFLAG_READ  <br/> |fmsRead  <br/> |
|MSGFLAG_UNMODIFED  <br/> |~fmsModified  <br/> |
|MSGFLAG_SUBMIT  <br/> |fmsSubmitted  <br/> |
|MSGFLAG_HASATTACH  <br/> |fmsHasAttach  <br/> |
|MSGFLAG_UNSENT  <br/> |fmsLocal  <br/> |
   
Ces indicateurs sont définis dans le TNEF. Fichier d’en-tête H.
  

