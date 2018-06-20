---
title: Centralisation de la réception de rapports de non-remise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0af587bd07de9445f143be316798059eaef402e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783028"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Centralisation de la réception de rapports de non-remise

**S’applique à**: Outlook 
  
**Pour que les rapports de non-remise (NDR) arrive à un emplacement central lorsque plusieurs instances de votre client exécutent simultanément**
  
1. Les valeurs appropriées pour le compte qui doit recevoir la valeur **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) et **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) les rapports. Créer l’identificateur d’entrée en appelant [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) si nécessaire. 
    
2. Comprendre les systèmes de messagerie qui ne tient pas compte le compte que vous avez demandé pour les rapports et les envoyez à l’expéditeur. Réduisez l’impact qu’il aura sur administrateurs que vous devrez déplacer les rapports :
    
- Donner à votre message d’origine à une classe de message distinctes, par exemple IPM. Note.MSNNews. Rechercher les messages entrants avec la classe Report.IPM.Note.MSNNews.NDR et les transférer vers le compte que vous avez l’intention de rapports placés au premier. En même temps, envoyer à un système de messagerie ignorée votre compte de rapport de non-remise pour communiquer qu’il doit respecter la propriété **PR_REPORT_ENTRYID** . 
    
- Les systèmes de messagerie plus qui n’effectue pas de **PR_REPORT_ENTRYID** pas respecte les conventions de classe de message MAPI soit. Par conséquent, vous serez invité à quelque chose qui ressemble à une note. Il s’agit d’un peu plus difficile à gérer, car l’entrée est donc variable. Examinez l’objet et le transmet si vous trouvez soit quelque chose à partir d’une liste de mots que moyenne « non remis » ou quelque chose à partir de l’objet d’origine. Préparez-vous à régler ces listes au fil du temps. 
    

