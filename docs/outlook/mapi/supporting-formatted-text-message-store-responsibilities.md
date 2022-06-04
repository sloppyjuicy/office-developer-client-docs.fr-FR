---
title: Prise en charge des responsabilités du magasin de messages texte mis en forme
description: Décrit la prise en charge des responsabilités du magasin de messages texte mis en forme. Cela s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
ms.openlocfilehash: f5c8b3ff89ed549e2ed24777771a30a5c478fd89
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894340"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Prise en charge du texte mis en forme : Responsabilités du magasin de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages utilisent la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour publier s’ils peuvent ou non gérer le format RTF (Rich Text Format), le texte HTML et, s’ils prennent en charge RTF, s’ils stockent le texte mis en forme dans un format compressé ou non compressé. Les fournisseurs de magasins de messages indiquent qu’ils prennent en charge RTF en définissant le bit STORE_RTF_OK et qu’ils stockent le texte mis en forme dans un formulaire non compressé en définissant le bit STORE_UNCOMPRESSED_RTF. Les fournisseurs de magasin de messages indiquent qu’ils prennent en charge html en définissant le STORE_HTML_OK bit.
  
Bien qu’il soit important qu’un client compatible RTF vérifie la STORE_RTF_OK bit pour déterminer si un magasin de messages prend en charge RTF, il n’est pas nécessaire qu’un client se préoccupe du format du texte mis en forme d’un magasin compatible RTF. 
  
Tous les magasins de messages doivent prendre en charge les clients qui ne prennent pas en charge RTF. Un magasin de messages non-RTF doit supprimer la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) lors d’un appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message si un client a modifié **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sans mettre à jour **PR_RTF_IN_SYNC** ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). La suppression **de PR_RTF_IN_SYNC** entraîne le recalcul de la propriété **PR_RTF_COMPRESSED** de la propriété **PR_BODY** la prochaine fois qu’un client qui prend en compte RTF appelle [RTFSync](rtfsync.md). 
  
La plupart des magasins de messages prenant en charge RTF ne reçoivent pas le texte du message par les clients ; il doit être calculé sur demande. Étant donné que ce calcul est long et coûteux, les clients doivent utiliser **PR_RTF_COMPRESSED** autant que possible. Pour calculer la propriété **PR_BODY** , le fournisseur de magasin de messages doit décompresser le contenu de la propriété **PR_RTF_COMPRESSED** et supprimer la mise en forme de texte enrichi. Les clients qui ne prennent pas en charge la propriété **PR_RTF_COMPRESSED** nécessitent ce calcul pour chaque message. 
  
Lors de la copie de messages, les fournisseurs de magasin de messages qui n’utilisent pas les méthodes **IMAPISupport::D oCopyProps** ou **IMAPISupport::D oCopyTo** courent le risque de créer un message sans contenu si leur implémentation exclut la propriété **PR_BODY** et s’appuie sur **PR_RTF_COMPRESSED**. Il est possible que les données de la propriété **PR_RTF_COMPRESSED** soient endommagées. Avant d’exclure l’une de ces propriétés de contenu de message dans l’opération de copie, recherchez l’altération comme suit : 
  
1. Si la valeur de **PR_RTF_COMPRESSED** n’est pas supérieure au RTF compressé, la propriété est endommagée. 
    
2. Si la valeur magique dans l’en-tête RTF n’est pas  _dwMagicCompressedRTF_ ou  _dwMagicUncompressedRTF_, la propriété est endommagée.
    
Les fournisseurs de magasins de messages qui utilisent les méthodes de support n’ont pas besoin d’être concernés par l’implémentation d’un contrôle de **PR_RTF_COMPRESSED** corruption ; MAPI garantit que les propriétés appropriées existent et sont valides. 
  
Il existe trois niveaux de prise en charge RTF différents que les fournisseurs de magasins de messages peuvent implémenter ; MAPI recommande que les fournisseurs de magasins de messages rtF implémentent leur prise en charge au niveau intermédiaire ou le plus élevé. Tous les fournisseurs de magasins de messages rtF s’occupent de générer **des PR_BODY** à partir des données incluses dans **PR_RTF_COMPRESSED** sur les messages sortants et d’appeler **RTFSync** pour synchroniser le texte et la mise en forme sur les messages entrants. 
  
Les différences entre ces trois niveaux sont décrites dans le tableau suivant. 
  
|**Niveau de prise en charge**|**Description**|
|:-----|:-----|
|Faible  <br/> |Le fournisseur du magasin de messages appelle **RTFSync** chaque fois que les modifications sont enregistrées dans un message et extrait les données de la propriété **PR_BODY** à partir de **PR_RTF_COMPRESSED** au lieu d’exiger des clients qu’ils le définissent. Les **PR_BODY** et **les PR_RTF_COMPRESSED** sont stockés. |
|Milieu  <br/> |Le fournisseur du magasin de messages stocke uniquement la propriété **PR_RTF_COMPRESSED** , en calculant **PR_BODY** si nécessaire. |
|Élevé  <br/> |Le fournisseur du magasin de messages ne stocke ni **PR_BODY** ni les propriétés RTF auxiliaires. **RTFSync** est appelé lorsque le texte du message a changé et que la mise en forme reste inchangée ou lorsqu’un nouveau message est téléchargé par un fournisseur de transport. |
   

