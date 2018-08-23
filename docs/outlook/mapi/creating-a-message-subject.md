---
title: Création d’un objet de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cae255b90e8f2ccaaec4736c7ba1e9d6b7764f58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593108"
---
# <a name="creating-a-message-subject"></a>Création d’un objet de message

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’objet d’un message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), est une propriété facultative, utilisée pour résumer l’objectif d’un message. Si vous choisissez de définir, rendre une chaîne de caractères 128 octets ou moins. La limite de 128 octets n’est pas une limite imposée par MAPI ; Il est une limite imposée par des fournisseurs de banque de messages. Pour garantir l’interopérabilité avec des fournisseurs qui imposent il, limiter les sujets à 128 octets. 
  
Sachez que certains fournisseurs de banque de messages ne permettent pas **PR_SUBJECT** est écrit dans un stream à l’interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
  
Ne définissez pas de **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) ; Cette propriété est définie uniquement sur les réponses et les messages transférée. 
  

