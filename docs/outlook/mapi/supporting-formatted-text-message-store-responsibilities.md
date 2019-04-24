---
title: Prise en charge des responsabilités de magasin de messages au format texte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 502ba82279664638c8e7e4ae68f74df74758918d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350679"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Prise en charge du texte mis en forme: responsabilités de la Banque de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de banques de messages utilisent la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour publier s'ils peuvent gérer le format RTF (Rich Text Format), le texte HTML et, s'ils sont compatibles avec le format RTF, s'ils stockent le texte mis en forme dans une balise format compressé ou non compressé. Les fournisseurs de banques de messages indiquent qu'ils peuvent prendre en charge le format RTF en définissant le bit STORE_RTF_OK et qu'ils stockent le texte mis en forme dans un formulaire non compressé en définissant le bit STORE_UNCOMPRESSED_RTF. Les fournisseurs de banques de messages indiquent qu'ils prennent en charge le langage HTML en définissant le bit STORE_HTML_OK.
  
Bien qu'il soit important pour un client compatible RTF de vérifier le bit STORE_RTF_OK pour déterminer si un magasin de messages prend en charge le format RTF, il n'est pas nécessaire qu'un client soit concerné par le format du texte mis en forme du magasin RTF. 
  
Tous les magasins de messages doivent prendre en charge les clients qui ne sont pas compatibles avec le format RTF. Un magasin de messages non compatible avec le format RTF doit supprimer la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) pendant un appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message si un client a modifié **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sans mise à jour de **PR_RTF_IN_SYNC** ou de **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). La suppression de **PR_RTF_IN_SYNC** entraîne le recalcul de la propriété **PR_RTF_COMPRESSED** à partir de la propriété **PR_BODY** la prochaine fois qu'un client compatible avec le format RTF appelle [RTFSync](rtfsync.md). 
  
La plupart des magasins de messages prenant en charge le format RTF ne reçoivent pas le texte du message par les clients; elle doit être calculée sur demande. Étant donné que ce calcul est onéreux et coûteux, les clients doivent utiliser **PR_RTF_COMPRESSED** chaque fois que cela est possible. Pour calculer la propriété **PR_BODY** , le fournisseur de banque de messages doit décompresser le contenu de la propriété **PR_RTF_COMPRESSED** et supprimer la mise en forme de texte enrichi. Les clients qui ne prennent pas en charge la propriété **PR_RTF_COMPRESSED** nécessitent que ce calcul ait lieu pour chaque message. 
  
Lors de la copie de messages, les fournisseurs de banques de messages qui n'utilisent pas les **IMAPISupport::D ocopyprops** ou **IMAPISupport::D ocopyto** méthodes exécutent le risque de créer un message sans contenu si leur implémentation exclut le **PR_BODY** propriété et s'appuie sur **PR_RTF_COMPRESSED**. Il est possible que les données de la propriété **PR_RTF_COMPRESSED** soient endommagées. Avant d'exclure l'une de ces propriétés de contenu de message dans l'opération de copie, vérifiez la corruption comme suit: 
  
1. Si la valeur de **PR_RTF_COMPRESSED** n'est pas supérieure au format RTF compressé, la propriété est endommagée. 
    
2. Si la valeur Magic de l'en-tête RTF n'est pas _dwMagicCompressedRTF_ ou _dwMagicUncompressedRTF_, la propriété est endommagée.
    
Les fournisseurs de banque de messages utilisant les méthodes de prise en charge n'ont pas besoin d'implémenter une vérification de l'endommagement **PR_RTF_COMPRESSED** ; MAPI garantit que les propriétés appropriées existent et sont valides. 
  
Il existe trois niveaux de prise en charge du format RTF que les fournisseurs de banques de messages peuvent implémenter; MAPI recommande que les fournisseurs de banques de messages prenant en charge le format RTF implémentent leur prise en charge au niveau le plus élevé ou au milieu. Tous les fournisseurs de banques de messages prenant en charge le format RTF sont en charge de la génération de **PR_BODY** à partir des données incluses dans **PR_RTF_COMPRESSED** sur les messages sortants et d'un appel à **RTFSync** pour synchroniser le texte et la mise en forme sur les messages entrants. 
  
Les différences entre ces trois niveaux sont décrites dans le tableau suivant. 
  
|**Niveau de prise en charge**|**Description**|
|:-----|:-----|
|Faible  <br/> |Le fournisseur de banque de messages appelle **RTFSync** chaque fois que des modifications sont enregistrées dans un message et extrait les données de la propriété **PR_BODY** à partir de **PR_RTF_COMPRESSED** au lieu de demander aux clients de le définir. **PR_BODY** et **PR_RTF_COMPRESSED** sont stockés.  <br/> |
|Centre  <br/> |Le fournisseur de banque de messages stocke uniquement la propriété **PR_RTF_COMPRESSED** , Computing **PR_BODY** si nécessaire.  <br/> |
|Importante  <br/> |Le fournisseur de banque de messages ne stocke ni **PR_BODY** ni les propriétés RTF auxiliaires. **RTFSync** est appelé lorsque le texte du message a changé et que la mise en forme reste inchangée ou lorsqu'un nouveau message est téléchargé par un fournisseur de transport.  <br/> |
   

