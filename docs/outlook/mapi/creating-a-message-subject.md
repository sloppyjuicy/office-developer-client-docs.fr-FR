---
title: Création d’un objet du Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 419c9776b380436b1a7163803a8677fb6a89be97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783118"
---
# <a name="creating-a-message-subject"></a>Création d’un objet du Message

  
  
**S’applique à**: Outlook 
  
L’objet d’un message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), est une propriété facultative, utilisée pour résumer l’objectif d’un message. Si vous choisissez de définir, rendre une chaîne de caractères 128 octets ou moins. La limite de 128 octets n’est pas une limite imposée par MAPI ; Il est une limite imposée par des fournisseurs de banque de messages. Pour garantir l’interopérabilité avec des fournisseurs qui imposent il, limiter les sujets à 128 octets. 
  
Sachez que certains fournisseurs de banque de messages ne permettent pas **PR_SUBJECT** est écrit dans un stream à l’interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
  
Ne définissez pas de **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) ; Cette propriété est définie uniquement sur les réponses et les messages transférée. 
  

