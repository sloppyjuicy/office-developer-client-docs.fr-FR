---
title: Création d'un objet de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332962"
---
# <a name="creating-a-message-subject"></a>Création d'un objet de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'objet d'un message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), est une propriété facultative, utilisée pour résumer l'objectif d'un message. Si vous choisissez de la définir, transmettez-la chaîne de caractères 128 octets ou moins. La limite de 128 octets n'est pas une limite imposée par MAPI; Il s'agit d'une limite imposée par certains fournisseurs de banques de messages. Pour garantir l'interopérabilité avec les fournisseurs qui l'imposent, limitez les objets à 128 octets. 
  
N'oubliez pas que certains fournisseurs de banques de messages ne permettent pas l'écriture de **PR_SUBJECT** dans un flux avec l'interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
  
Ne pas définir **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Cette propriété est définie uniquement sur les réponses et les messages transférés. 
  

