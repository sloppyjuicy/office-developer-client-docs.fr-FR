---
title: Validation et initialisation d’une banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7a5a5045594e87953d967fddbdeefd5ac18c8a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581971"
---
# <a name="validating-and-initializing-a-message-store"></a>Validation et initialisation d’une banque de messages

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsque vous ouvrez une banque de messages par le biais de la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sans définir l’indicateur MDB_NO_MAIL, MAPI crée plusieurs dossiers et attribue les rôles et les noms par défaut. MAPI est responsable de la création de ces dossiers pour éviter les incompatibilités inévitablement cas de clients ou fournisseurs de banque de message ont été responsables de la création. 
  
Il est parfois nécessaire de vérifier que les dossiers appropriés ont été créés et qu’ils sont valides. La fonction [HrValidateIPMSubtree](hrvalidateipmsubtree.md) est disponible à cet effet. Si vous validez la banque de messages par défaut, passez l’indicateur MAPI_FULL_IPM_TREE. Un groupe de dossiers plus étendu est créé pour la banque de messages par défaut. Lorsque **HrValidateIPMSubtree** reçoit l’indicateur MAPI_FULL_IPM_TREE, il recherche les dossiers suivants : 
  
- Dossier racine de la sous-arborescence IPM
    
- Dossier éléments supprimés dans le dossier racine IPM
    
- Dossier boîte de réception dans le dossier racine IPM
    
- Dossier dans le dossier racine IPM boîte d’envoi
    
- Dossier éléments envoyés dans le dossier racine IPM
    
- Vues de dossiers dans le dossier racine de la banque messages
    
- Affichages courantes dans le dossier racine de la banque messages
    
- Dossier de recherche dans le dossier racine de la banque messages
    
Si la banque de messages n’est pas la valeur par défaut, vous pouvez définir ou pas définir l’indicateur MAPI_FULL_IPM_TREE. Lorsque cet indicateur n’est pas défini, **HrValidateIPMSubtree** vérifie uniquement le dossier racine de la sous-arborescence, le dossier éléments supprimés et le dossier racine de message stockent les résultats de la recherche. 
  
Pour initialiser une banque de messages, stocker les propriétés suivantes dans la mémoire, afin qu’ils soient disponibles :
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Ces propriétés sont des masques de bits qui décrivent les fonctionnalités de la banque de messages. **PR_VALID_FOLDER_MASK** a un bit défini pour chaque dossier spécial qui existe dans la banque de messages et possède un identificateur d’entrée affecté est valid. Pour plus d’informations sur l’accès à ces dossiers et leurs identificateurs d’entrée, voir [l’ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md). 
  
 **PR_STORE_SUPPORT_MASK** a un bit défini pour toutes les fonctionnalités prises en charge dans la banque de messages. Par exemple, si une banque de messages prend en charge les notifications et texte mis en forme, sa **PR_STORE_SUPPORT_MASK** auront l’ensemble de bits STORE_NOTIFY_OK et STORE_RTF_OK. 
  
Autres propriétés qui doivent être stockées localement incluent les identificateurs d’entrée pour les dossiers que la propriété **PR_VALID_FOLDER_MASK** décrit comme étant valide. Chacun de ces dossiers spéciaux, à l’exception du dossier boîte de réception, a une propriété identificateur associée. Par exemple, l’identificateur d’entrée pour le dossier boîte d’envoi est sa propriété **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). Étant donné que ces dossiers sont les dossiers qui seront ouverts fréquemment, il est préférable de leurs identificateurs d’entrée disponibles.
  

