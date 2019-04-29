---
title: Validation et initialisation d'une banque de messages
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
# <a name="validating-and-initializing-a-message-store"></a>Validation et initialisation d'une banque de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous ouvrez une banque de messages à l'aide de la méthode [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) sans définir l'indicateur MDB_NO_MAIL, MAPI crée plusieurs dossiers et leur affecte des noms et des rôles par défaut. MAPI est responsable de la création de ces dossiers pour éviter les incompatibilités qui se produisent inévitablement si les clients ou les fournisseurs de banques de messages étaient responsables de la création. 
  
Parfois, il est nécessaire de vérifier que les dossiers appropriés ont été créés et qu'ils sont valides. La fonction [HrValidateIPMSubtree](hrvalidateipmsubtree.md) est disponible à cette fin. Si vous validez la Banque de messages par défaut, transmettez l'indicateur MAPI_FULL_IPM_TREE. Un groupe de dossiers plus complet est créé pour la Banque de messages par défaut. Lorsque **HrValidateIPMSubtree** reçoit l'indicateur MAPI_FULL_IPM_TREE, il recherche les dossiers suivants: 
  
- Dossier racine de la sous-arborescence IPM
    
- Dossier éléments supprimés dans le dossier racine IPM
    
- Dossier boîte de réception dans le dossier racine IPM
    
- Dossier boîte d'envoi dans le dossier racine IPM
    
- Dossier éléments envoyés dans le dossier racine IPM
    
- Affichages de dossiers dans le dossier racine de la Banque de messages
    
- Affichages courants dans le dossier racine de la Banque de messages
    
- Dossier de recherche dans le dossier racine de la Banque de messages
    
Si la Banque de messages n'est pas la valeur par défaut, vous pouvez définir ou ne pas définir l'indicateur MAPI_FULL_IPM_TREE. Lorsque cet indicateur n'est pas défini, **HrValidateIPMSubtree** recherche uniquement le dossier racine de la sous-arborescence, le dossier éléments supprimés et le dossier racine des résultats de recherche de la Banque de messages. 
  
Pour initialiser une banque de messages, stockez les propriétés suivantes dans la mémoire afin qu'elles soient immédiatement disponibles:
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Ces propriétés sont des masques de masques qui décrivent les fonctionnalités de la Banque de messages. **PR_VALID_FOLDER_MASK** possède un bit défini pour chaque dossier spécial qui existe dans la Banque de messages et dont l'identificateur d'entrée est valide. Pour plus d'informations sur l'accès à ces dossiers et leurs identificateurs d'entrée, voir [ouverture d'un dossier de la Banque de messages](opening-a-message-store-folder.md). 
  
 **PR_STORE_SUPPORT_MASK** possède un bit défini pour chaque fonctionnalité prise en charge dans la Banque de messages. Par exemple, si un magasin de messages prend en charge la notification et le texte mis en forme, les bits STORE_NOTIFY_OK et STORE_RTF_OK seront définis pour ses **PR_STORE_SUPPORT_MASK** . 
  
Les autres propriétés qui doivent être stockées localement incluent les identificateurs d'entrée pour les dossiers décrits par la propriété **PR_VALID_FOLDER_MASK** comme étant valide. Chacun de ces dossiers spéciaux, à l'exception du dossier boîte de réception, possède une propriété d'identificateur d'entrée qui lui est associée. Par exemple, l'identificateur d'entrée pour le dossier boîte d'envoi est sa propriété **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). Étant donné que ces dossiers sont les dossiers qui seront ouverts fréquemment, il est recommandé d'avoir leurs identificateurs d'entrée immédiatement disponibles.
  

