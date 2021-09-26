---
title: Création d’un objet de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b5ae0c8e16af35b730d6a1fbdcf95b74c6119e1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631070"
---
# <a name="creating-a-message-subject"></a>Création d’un objet de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’objet d’un message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), est une propriété facultative, utilisée pour résumer l’intention d’un message. Si vous choisissez de la définir, faites-en une chaîne de caractères de 128 octets ou moins. La limite de 128 byte n’est pas une limite imposée par MAPI ; Il s’agit d’une limite imposée par certains fournisseurs de magasins de messages. Pour garantir l’interopérabilité avec les fournisseurs qui l’imposent, limitez les sujets à 128 octets. 
  
Sachez que certains fournisseurs de magasins de messages n’autorisent **pas PR_SUBJECT’écriture** dans un flux avec [l’interface IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
  
Ne définissez **pas PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) ; cette propriété est définie uniquement sur les réponses et les messages transmis. 
  

