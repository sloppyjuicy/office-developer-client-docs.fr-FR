---
title: Création d’un objet de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
ms.openlocfilehash: 6a098d2c6c26e3ee2f0a885ad9c17657a4f18b6e
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370090"
---
# <a name="creating-a-message-subject"></a>Création d’un objet de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’objet d’un message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), est une propriété facultative, utilisée pour résumer l’intention d’un message. Si vous choisissez de la définir, faites-en une chaîne de caractères de 128 octets ou moins. La limite de 128 byte n’est pas une limite imposée par MAPI ; Il s’agit d’une limite imposée par certains fournisseurs de magasins de messages. Pour garantir l’interopérabilité avec les fournisseurs qui l’imposent, limitez les sujets à 128 octets. 
  
Sachez que certains fournisseurs de magasins de messages n’autorisent **pas PR_SUBJECT’écriture** dans un flux avec l’interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
  
Ne définissez **pas PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) ; cette propriété est définie uniquement sur les réponses et les messages transmis. 
  

