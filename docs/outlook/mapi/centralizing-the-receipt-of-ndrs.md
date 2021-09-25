---
title: Centralisation de la réception des notifications d’échec de remise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9df0229a34e26dc0a40b6405a53b71421f79d877
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551813"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Centralisation de la réception des notifications d’échec de remise

**S’applique à** : Outlook 2013 | Outlook 2016 
  
**Pour que les rapports de non-delivery arrivent à un emplacement central lorsque plusieurs instances de votre client s’exécutent simultanément**
  
1. Définissez **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) et **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) sur les valeurs appropriées pour le compte qui doit recevoir les rapports. Créez l’identificateur d’entrée en appelant [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) si nécessaire. 
    
2. Comprenez qu’il existe des systèmes de messagerie qui ignorent le compte que vous avez demandé pour les rapports et les envoient à l’expéditeur. Réduisez l’impact que cela aura sur les administrateurs qui devront déplacer des rapports par :
    
- Donner à votre message d’origine une classe de message distincte, telle qu’IPM. Note.MSNNews. Recherchez les messages entrants avec class Report.IPM.Note.MSNNews.NDR et transfertz-les vers le compte vers qui vous souhaitez envoyer des rapports. En même temps, envoyez un courrier électronique au système de messagerie qui a ignoré votre compte de rapport de non-envoi pour signaler qu’il doit respecter la **propriété PR_REPORT_ENTRYID.** 
    
- La plupart des systèmes de messagerie qui ne respectent **pas PR_REPORT_ENTRYID** respectent pas non plus les conventions de classe de message MAPI. Par conséquent, vous recevrez un message qui ressemble à une note. Cette opération est un peu plus difficile à gérer, car l’entrée est très variable. Regardez l’objet et faites-le avancer si vous trouvez quelque chose dans une liste de mots qui signifie « non transmis » ou quelque chose de votre objet d’origine. Soyez prêt à régler ces listes au fil du temps. 
    

