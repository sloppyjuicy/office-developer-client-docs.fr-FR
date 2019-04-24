---
title: Prise en charge du texte RTF pour les fournisseurs de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349615"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Prise en charge du texte RTF pour les fournisseurs de banque de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certaines applications clientes permettent aux utilisateurs d'utiliser du texte RTF (Rich Text Format) dans leurs messages. Si votre fournisseur de banque de messages doit prendre en charge le texte RTF dans les messages, il doit gérer la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), en plus de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). En premier lieu, cela signifie de stocker les deux propriétés et de s'assurer que **PR_BODY** contient une version en texte brut du texte dans **PR_RTF_COMPRESSED**. La fonction [RTFSync](rtfsync.md) est utile à cette fin. 
  
Deux indicateurs peuvent être définis dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l'objet Banque de messages qui indique aux clients ce qu'ils peuvent attendre du fournisseur de banque de messages par rapport au **PR_BODY** et à **PR_ Propriétés RTF_COMPRESSED** sur les messages dans la Banque de messages. L'indicateur STORE_RTF_OK indique que la Banque peut générer de manière dynamique la valeur de la propriété **PR_BODY** à partir de la propriété **PR_RTF_COMPRESSED** , ce qui évite aux clients de procéder à leur synchronisation de manière explicite. L'indicateur STORE_UNCOMPRESSED_RTF indique que le fournisseur de banque de messages peut prendre en charge des données non compressées dans **PR_RTF_COMPRESSED**.
  
Les fournisseurs de banques de messages qui ne prennent pas en charge le texte RTF doivent supprimer la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) lorsque la propriété **PR_BODY** est modifiée afin d'interagir correctement avec les applications clientes qui prennent en charge le texte RTF . 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

