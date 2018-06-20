---
title: Prise en charge des responsabilités de la banque de messages texte mis en forme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 301ebbf8e7a3e2a2deb303af5b198fd11511d495
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787272"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Prenant en charge le format texte : Responsabilités de banque de messages

  
  
**S’applique à**: Outlook 
  
Fournisseurs de banque de messages **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) la propriété permet pour publier ou non ils peuvent gérer le texte enrichi (RTF), le texte HTML et, si elles sont au format RTF prenant en charge, si elles stockent le texte mis en forme dans un format compressé ou non compressé. Fournisseurs de magasins de message indiquent qu’ils sont compatibles RTF en définissant le bit STORE_RTF_OK et qu’elles contiennent le texte mis en forme dans un formulaire non compressé en définissant le bit STORE_UNCOMPRESSED_RTF. Fournisseurs de magasins de message indiquent qu’ils sont compatibles HTML en définissant le bit STORE_HTML_OK.
  
S’il est important pour un client prenant en charge au format RTF vérifier la STORE_RTF_OK bit pour déterminer si une banque de messages prend en charge le format RTF, il n’est pas nécessaire pour qu’un client concernés avec le format de texte mis en forme d’un magasin de RTF prenant en charge. 
  
Tous les magasins de message doivent prendre en charge les clients non compatibles RTF. Une banque de messages non compatible RICH doit supprimer la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) pendant un appel à la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message, si un client a été modifiée **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sans mise à jour de le **PR_RTF_IN_SYNC** ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Suppression de **PR_RTF_IN_SYNC** , la propriété **PR_RTF_COMPRESSED** recalculé à partir de la propriété **PR_BODY** la prochaine fois qu’un client prenant en charge les RTF appelle [RTFSync](rtfsync.md). 
  
La plupart des banques de messages RTF prenant en charge ne figurent pas le texte du message par les clients ; Il doit être calculée à la demande. Ce calcul étant fastidieuse et coûteuse, les clients doivent utiliser **PR_RTF_COMPRESSED** autant que possible. Pour calculer la propriété **PR_BODY** , le fournisseur de banque de message doit décompresser le contenu de la propriété **PR_RTF_COMPRESSED** et supprimer la mise en forme de texte enrichi. Les clients qui ne prennent pas en charge la propriété **PR_RTF_COMPRESSED** nécessitent ce calcul s’effectuent pour chaque message. 
  
Lors de la copie des messages, les fournisseurs qui n’utilisent pas les méthodes **IMAPISupport::DoCopyProps** ou **IMAPISupport::DoCopyTo** courez le risque de création d’un message sans contenu si leur mise en œuvre exclut le **PR_BODY** banque de messages propriété et s’appuie sur **PR_RTF_COMPRESSED**. Il est possible pour les données dans la propriété **PR_RTF_COMPRESSED** est endommagé. Avant d’une de ces propriétés de contenu de message dans l’opération de copie exclure, vérifiez le comme suit : 
  
1. Si la valeur de **PR_RTF_COMPRESSED** n’est pas supérieure à du texte RTF compressé, la propriété est endommagée. 
    
2. Si la valeur magique dans l’en-tête du format RTF n’est pas _dwMagicCompressedRTF_ ou _dwMagicUncompressedRTF_, la propriété est endommagé.
    
Banque de messages fournisseurs à l’aide de la prise en charge des méthodes ne doivent ne pas être concernées par la mise en œuvre d’une vérification est endommagé **PR_RTF_COMPRESSED** ; MAPI garantit que les propriétés appropriées existent et sont valides. 
  
Il existe trois différents niveaux de prise en charge au format RTF peuvent implémentés par les fournisseurs de banque de messages ; MAPI recommande que les fournisseurs de magasins message RTF prenant en charge implémentent leur prise en charge au niveau du milieu ou la plus élevé. Tous les prenant en charge les RTF banque de messages fournisseurs de prendre en charge de la génération de **PR_BODY** à partir de données incluses dans **PR_RTF_COMPRESSED** sur les messages sortants et émettre un appel à **RTFSync** pour synchroniser le texte et la mise en forme dans les messages entrants. 
  
Les différences entre ces trois niveaux sont décrits dans le tableau suivant. 
  
|**Niveau de prise en charge**|**Description**|
|:-----|:-----|
|Low  <br/> |Message stocker fournisseur appelle **RTFSync** chaque fois que les modifications sont enregistrées dans un message et extrait les données de la propriété **PR_BODY** de **PR_RTF_COMPRESSED** plutôt que des clients nécessitant qu’elle. Les **PR_BODY** et **PR_RTF_COMPRESSED** sont stockées.  <br/> |
|Milieu  <br/> |Message stocker les magasins de fournisseur que la propriété **PR_RTF_COMPRESSED** informatique **PR_BODY** lorsque cela est nécessaire.  <br/> |
|High  <br/> |Message stocker les magasins de fournisseur ni **PR_BODY** , ni les propriétés RTF auxiliaires. **RTFSync** est appelé lorsque le texte du message a été modifié et la mise en forme reste inchangée ou lorsqu’un nouveau message est téléchargé par un fournisseur de transport.  <br/> |
   

