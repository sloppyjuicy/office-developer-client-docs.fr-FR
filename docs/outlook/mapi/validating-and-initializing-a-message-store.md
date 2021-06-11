---
title: Validation et initialisation d’une magasin de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433688"
---
# <a name="validating-and-initializing-a-message-store"></a>Validation et initialisation d’une magasin de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous ouvrez une magasin de messages via la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sans définir l’indicateur MDB_NO_MAIL, MAPI crée plusieurs dossiers et leur attribue des noms et des rôles par défaut. MAPI est responsable de la création de ces dossiers afin d’éviter les incompatibilités qui seraient inévitablement présentes si les clients ou les fournisseurs de magasins de messages étaient responsables de la création. 
  
Il est parfois nécessaire de vérifier que les dossiers appropriés ont été créés et qu’ils sont valides. La [fonction HrValidateIPMSubtree](hrvalidateipmsubtree.md) est disponible à cet effet. Si vous validez la boutique de messages par défaut, passez l’MAPI_FULL_IPM_TREE message. Un groupe plus étendu de dossiers est créé pour la magasin de messages par défaut. Lorsque **HrValidateIPMSubtree** reçoit l’indicateur MAPI_FULL_IPM_TREE, il recherche les dossiers suivants : 
  
- Dossier racine de la sous-arbre IPM
    
- Dossier Éléments supprimés dans le dossier racine IPM
    
- Dossier boîte de réception dans le dossier racine IPM
    
- Dossier boîte d’envoi dans le dossier racine IPM
    
- Dossier Éléments envoyés dans le dossier racine IPM
    
- Affichages des dossiers dans le dossier racine de la boutique de messages
    
- Affichages communs dans le dossier racine de la boutique de messages
    
- Dossier de recherche dans le dossier racine de la boutique de messages
    
Si la magasin de messages n’est pas la valeur par défaut, vous pouvez définir ou non l’MAPI_FULL_IPM_TREE de message. Lorsque cet indicateur n’est pas définie, **HrValidateIPMSubtree** vérifie uniquement le dossier racine de la sous-arbre, le dossier Éléments supprimés et le dossier racine pour les résultats de recherche de la magasin de messages. 
  
Pour initialiser une magasin de messages, stockez les propriétés suivantes en mémoire afin qu’elles soient facilement disponibles :
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Ces propriétés sont des masques de bits qui décrivent les fonctionnalités de la boutique de messages. **PR_VALID_FOLDER_MASK** a un bit pour chaque dossier spécial qui existe dans la boutique de messages et possède un identificateur d’entrée attribué valide. Pour plus d’informations sur l’accès à ces dossiers et à leurs identificateurs d’entrée, voir [Ouverture d’un dossier de la boutique de messages.](opening-a-message-store-folder.md) 
  
 **PR_STORE_SUPPORT_MASK** a un bit pour chaque fonctionnalité prise en charge dans la boutique de messages. Par exemple, si une magasin de messages  prend en charge les notifications et le texte mis en forme, son PR_STORE_SUPPORT_MASK les bits STORE_NOTIFY_OK et STORE_RTF_OK sont définies. 
  
Les autres propriétés qui doivent être stockées localement incluent les identificateurs d’entrée pour les dossiers que la **propriété PR_VALID_FOLDER_MASK** décrit comme valides. Chacun de ces dossiers spéciaux, à l’exception du dossier Boîte de réception, est associé à une propriété d’identificateur d’entrée. Par exemple, l’identificateur d’entrée du dossier Outbox est **PR_IPM_OUTBOX_ENTRYID** propriété ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). Étant donné que ces dossiers sont les dossiers qui seront ouverts fréquemment, il est bon d’avoir leurs identificateurs d’entrée facilement disponibles.
  

