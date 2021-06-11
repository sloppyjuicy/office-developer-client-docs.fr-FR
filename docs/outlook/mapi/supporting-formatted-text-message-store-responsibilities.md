---
title: Prise en charge des responsabilités du magasin de messages texte formatés
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 502ba82279664638c8e7e4ae68f74df74758918d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435515"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Prise en charge du texte formaté : responsabilités de la boutique de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages utilisent la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour publier s’ils peuvent gérer le format RTF (Rich Text Format), le texte HTML et, s’ils sont sensibles au format RTF, s’ils stockent le texte mis en forme dans un format compressé ou non. Les fournisseurs de magasins de messages indiquent qu’ils sont sensibles au format RTF en STORE_RTF_OK bits et qu’ils stockent le texte mis en forme dans un formulaire non compressé en STORE_UNCOMPRESSED_RTF bit. Les fournisseurs de magasins de messages indiquent qu’ils sont au format HTML en STORE_HTML_OK bit.
  
Bien qu’il soit important qu’un client au format RTF vérifie si le bit STORE_RTF_OK est pris en charge par une magasin de messages, il n’est pas nécessaire qu’un client soit concerné par le format du texte formaté d’un magasin rtf. 
  
Toutes les magasins de messages doivent prendre en charge les clients non rtF. Une magasin de messages non RTF doit supprimer la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) lors d’un appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message si un client a modifié **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sans mettre à jour **PR_RTF_IN_SYNC** ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). La suppression **PR_RTF_IN_SYNC** entraîne la recompilation de la propriété **PR_RTF_COMPRESSED** à partir de la propriété **PR_BODY** la prochaine fois qu’un client rtF appelle [RTFSync](rtfsync.md). 
  
La plupart des magasins de messages rtF ne sont pas informés du texte du message par les clients . Il doit être calculé sur demande. Étant donné que ce calcul est long et coûteux, les clients doivent utiliser **PR_RTF_COMPRESSED** chaque fois que possible. Pour calculer la **propriété PR_BODY,** le fournisseur de magasins de messages doit décompresser le contenu de la propriété **PR_RTF_COMPRESSED** et supprimer la mise en forme de texte enrichi. Les clients qui ne prennent pas **en charge la propriété PR_RTF_COMPRESSED** nécessitent ce calcul pour chaque message. 
  
Lors de la copie de messages, les fournisseurs de magasins de messages qui n’utilisent pas les méthodes **IMAPISupport::D oCopyProps** ou **IMAPISupport::D oCopyTo** risquent de créer un message sans contenu si leur implémentation exclut la propriété **PR_BODY** et s’appuie sur **PR_RTF_COMPRESSED**. Il est possible que les données de la **propriété PR_RTF_COMPRESSED** soient endommagées. Avant d’exclure l’une de ces propriétés de contenu de message dans l’opération de copie, vérifiez la corruption comme suit : 
  
1. Si la valeur de **PR_RTF_COMPRESSED** n’est pas supérieure à la valeur RTF compressée, la propriété est endommagée. 
    
2. Si la valeur magique dans l’en-tête RTF n’est  _pas dwMagicCompressedRTF_ ou  _dwMagicUncompressedRTF,_ la propriété est endommagée.
    
Les fournisseurs de magasins de messages qui utilisent les méthodes de support ne doivent pas se préoccuper de l’implémentation d’une vérification **de l’PR_RTF_COMPRESSED** corruption ; MAPI garantit que les propriétés appropriées existent et sont valides. 
  
Les fournisseurs de magasins de messages peuvent implémenter trois niveaux de prise en charge RTF différents ; MAPI recommande aux fournisseurs de magasins de messages rtF d’implémenter leur prise en charge au niveau intermédiaire ou supérieur. Tous les fournisseurs de magasins de messages rtF prennent en charge la génération de **PR_BODY** à partir des données incluses dans les messages sortants **PR_RTF_COMPRESSED** et appellent **RTFSync** pour synchroniser le texte et la mise en forme sur les messages entrants. 
  
Les différences entre ces trois niveaux sont décrites dans le tableau suivant. 
  
|**Niveau de prise en charge**|**Description**|
|:-----|:-----|
|Faible  <br/> |Le fournisseur de magasin de messages appelle **RTFSync** chaque fois que les modifications sont enregistrées dans un message et extrait les données de la propriété **PR_BODY** à partir de **PR_RTF_COMPRESSED** au lieu d’obliger les clients à les définir. Les **PR_BODY** et **PR_RTF_COMPRESSED** sont stockés.  <br/> |
|Milieu  <br/> |Le fournisseur de magasins de messages stocke uniquement **la propriété PR_RTF_COMPRESSED,** en calculant **PR_BODY** si nécessaire.  <br/> |
|Élevé  <br/> |Le fournisseur de magasins de messages **ne stocke PR_BODY** ou les propriétés RTF auxiliaires. **RTFSync** est appelé lorsque le texte du message a changé et que la mise en forme reste inchangée ou lorsqu’un nouveau message est téléchargé par un fournisseur de transport.  <br/> |
   

