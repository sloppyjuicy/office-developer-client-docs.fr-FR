---
title: Prise en charge de texte RTF pour les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3e65ebd3ea485ca54978d622e8aaf093dc5eff74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594067"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Prise en charge de texte RTF pour les fournisseurs de banques de messages

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Certaines applications de client permettent aux utilisateurs d’utiliser le texte RTF (RICH Text Format) dans leurs messages. Si votre message stocker le fournisseur doit prendre en charge de texte RTF dans les messages, il doit gérer la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), en plus de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Cela signifie principalement, stockant les deux propriétés et à s’assurer que **PR_BODY** contient une version en texte brut du texte **PR_RTF_COMPRESSED**. La fonction [RTFSync](rtfsync.md) est utile à cet effet. 
  
Il existe deux indicateurs peuvent être définies dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l’objet de banque de messages qui indiquent les clients à ce qu’ils attendent à partir du fournisseur de magasin de message en ce qui concerne les **PR_BODY** et **PR_ RTF_COMPRESSED** propriétés sur les messages dans la banque de messages. L’indicateur STORE_RTF_OK indique que le magasin peut générer la valeur de la propriété **PR_BODY** à partir de la propriété **PR_RTF_COMPRESSED** dynamiquement, qui permet de clients à partir de la charge de la synchronisation explicitement. L’indicateur STORE_UNCOMPRESSED_RTF indique que le fournisseur de banque de message peut prendre en charge des données non compressées dans **PR_RTF_COMPRESSED**.
  
Les fournisseurs de magasins de message qui ne prennent pas en charge le texte RTF nécessaire de supprimer la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) lorsque la propriété **PR_BODY** change afin de fonctionner correctement avec les applications clientes qui ne prennent pas en charge le texte RTF . 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

