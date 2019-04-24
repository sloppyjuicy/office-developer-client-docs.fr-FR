---
title: Centralisation de la réception des notifications d’échec de remise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332661"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Centralisation de la réception des notifications d’échec de remise

**S’applique à** : Outlook 2013 | Outlook 2016 
  
**Pour que les rapports de non-remise (NDR) arrivent à un emplacement central lorsque plusieurs instances de votre client fonctionnent simultanément**
  
1. Définissez **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) et **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) sur les valeurs appropriées pour le compte à recevoir. les rapports. Créez l'identificateur d'entrée en appelant [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) si nécessaire. 
    
2. SaChez qu'il existe des systèmes de messagerie qui ignorent le compte que vous avez demandé pour les rapports et les envoie à l'expéditeur. Réduisez l'impact que cela aura sur les administrateurs qui devront déplacer des rapports en procédant comme suit:
    
- Donner à votre message d'origine une classe de message distincte, telle que IPM. Note. MSNNews. Recherchez les messages entrants avec la classe Report. IPM. note. MSNNews. NDR et transférez-les vers le compte auquel vous avez prévu des rapports. En même temps, envoyez un message électronique au système de messagerie qui a ignoré votre compte de notification de remise indisponible pour communiquer qu'il doit honorer la propriété **PR_REPORT_ENTRYID** . 
    
- La plupart des systèmes de messagerie qui ne respectent pas **PR_REPORT_ENTRYID** n'honoreront pas les conventions de classe de message MAPI. Par conséquent, vous recevrez un message ressemblant à une note. Il s'agit d'un peu plus difficile à traiter car l'entrée est tellement variable. Examinez l'objet et transférez-le si vous trouvez un article dans une liste de mots signifiant «non remis» ou un autre sujet de votre objet d'origine. Soyez prêt à ajuster ces listes au fil du temps. 
    

